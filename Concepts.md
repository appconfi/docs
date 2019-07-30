
# Concepts

### Application 

Applications are the essential bit for **Appconfi**. It is the container for your application settings and feature toggles. You can have several applications based on your needs.

### Environments

Environments allows you to create more complex configurations for you applications. Create as many environments as you need, for example <em>PRODUCTION</em> or <em>TESTING</em>.

### Settings

Your applications will often require data that is critical to running the application, but which you do not want to include directly in the application's code. With **Appconfi** application settings, you can store not only application data such as database connection strings, but also user-specific data, such as user application preferences.  

### Feature toggle

Feature toggles, allow teams to modify system behavior without changing code. For more information about this pattern you can read this [article](https://martinfowler.com/articles/feature-toggles.html).
