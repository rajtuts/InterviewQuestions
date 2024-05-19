***Explain the difference between update and merge methods in hibernate with example?***

Here's a breakdown of the differences between `update` and `merge` methods in Hibernate, along with an example to illustrate their behavior:

**Update**

* Used to update an **already persistent** object in the database.
* The object must be loaded from the session using methods like `get` or `load` before using `update`.
* Throws an exception (`NonUniqueObjectException`) if another object with the same identifier already exists in the session.
* More efficient if you're certain the object is already managed.

**Merge**

* Works with **detached objects** (objects not currently associated with a session).
* Can be used regardless of whether the object exists in the session or not.
* If the object exists in the session, `merge` updates the existing object with the changes from the detached object.
* If the object doesn't exist, `merge` makes the detached object persistent.
* More versatile but might cause additional database interactions to check for existing objects.

**Example:**

Imagine you have a `Product` object with an identifier (`id`) and a name.

```java
Product product = session.get(Product.class, 10); // Load from database (persistent)
product.setName("New Name");

// Update scenario (object already loaded)
session.update(product);

// Merge scenario (object might or might not be loaded)
Product detachedProduct = new Product(10, "Modified Name"); // Detached object
Product mergedProduct = session.merge(detachedProduct);

// Now both product and mergedProduct reference the updated product in the database
```

**In summary:**

* Use `update` when you know the object is already managed and want a potentially faster update.
* Use `merge` when you're unsure about the object's state or want to handle both detached and attached object updates in a single method.

***Provide an example when NonUniqueObjectException throws when using hibernate update method?***


Here's an example of how you might encounter a `NonUniqueObjectException` when using the `update` method in Hibernate:

```java
// Scenario 1: Modifying two loaded objects with the same ID

Session session = sessionFactory.openSession();
session.beginTransaction();

Product product1 = session.get(Product.class, 1); // Load product with ID 1 (persistent)
Product product2 = session.get(Product.class, 1); // Load the same product again (persistent)

product1.setName("Updated Name 1");
product2.setName("Updated Name 2");

// Attempting to update product1 throws the exception
session.update(product1); // Throws NonUniqueObjectException

session.getTransaction().rollback();
session.close();
```

In this scenario, both `product1` and `product2` represent the same product in the database (ID 1) but are loaded into the session separately. When you try to update `product1`, Hibernate detects another object with the same identifier (`product2`) already associated with the session and throws the `NonUniqueObjectException` to prevent potential data inconsistencies.

Here's another scenario:

```java
// Scenario 2: Saving a detached object with an existing ID

Session session = sessionFactory.openSession();
session.beginTransaction();

Product product = new Product(2, "New Product"); // Detached object

// This will save the product (persistent)
session.save(product);

// Now trying to update the same product using update throws the exception
product.setName("Modified Name");
session.update(product); // Throws NonUniqueObjectException

session.getTransaction().rollback();
session.close();
```

Here, you first save a new `product` with ID 2. Then, you try to update the same product using `update`. Since the object wasn't loaded from the session initially (detached), Hibernate attempts to treat it as a new update, but the ID already exists. This again leads to the `NonUniqueObjectException`. 
