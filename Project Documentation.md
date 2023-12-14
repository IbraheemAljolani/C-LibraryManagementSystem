## Project Documentation

### Design Choices:

1. **Base Class (`Entity`):**
   - Represents the fundamental structure for entities within the management system.
   - Contains basic attributes such as `name` and `id`.
   - Provides a virtual method `display()` for displaying entity information.
   - Overloads the equality operator (`==`) to compare entities based on their IDs.

2. **Generic Management System (`ManagementSystem` Template Class):**
   - Serves as the base class for specific management systems (e.g., Library Management System, Inventory Management System).
   - Implements generic functionalities, including adding, displaying, and finding entities within the system.
   - Utilizes templates to allow flexibility in managing different types of entities.

3. **Domain-Specific Classes (`Book` and `Product`):**
   - Derived from the `Entity` base class to represent entities specific to the chosen domains (Library and Inventory).
   - Include additional attributes and methods relevant to each domain (e.g., author and availability for books, price and quantity for products).
   - Overload the `display()` method to provide domain-specific information.

4. **Composition for Management Systems:**
   - Utilizes composition to manage collections of entities within each management system.
   - `LibraryManagementSystem` composes a collection of `Book` objects.
   - `InventoryManagementSystem` composes a collection of `Product` objects.

5. **Command-Line User Interface:**
   - Implements a simple command-line interface for user interaction.
   - Allows users to add, remove, and display information related to the chosen domain (Library or Inventory).

### Key Functionalities:

1. **Adding Entities:**
   - Users can add new entities (books or products) to the respective management systems through the command-line interface.
   - Overloaded constructors facilitate the initialization of entities with user-provided information.

2. **Removing Entities:**
   - Users can remove entities by providing the entity ID through the command-line interface.
   - Overloaded methods (`removeBookById` and `removeProductById`) remove the specified entity from the system.

3. **Displaying Entities:**
   - Users can display the current contents of the chosen management system.
   - Overloaded `display()` methods provide domain-specific information for each entity.

4. **Overloading Operators:**
   - The `Entity` base class overloads the equality operator (`==`) for comparing entities based on their IDs.
   - The `Book` class overloads the addition operator (`+`) to demonstrate domain-specific behavior (combining authors).
   - The `Product` class overloads the multiplication operator (`*`) to demonstrate domain-specific behavior (increasing quantity).

### Utilization of Overloading, Composition, and Inheritance:

1. **Overloading:**
   - Overloaded constructors are used to provide default values and initialize entities with user-provided information.
   - The equality operator is overloaded in the `Entity` class for comparing entities based on their IDs.
   - The addition operator is overloaded in the `Book` class to combine authors when adding books.
   - The multiplication operator is overloaded in the `Product` class to increase quantity when multiplying by an integer.

2. **Composition:**
   - Composition is utilized to manage collections of entities within each management system.
   - `LibraryManagementSystem` composes a collection of `Book` objects, and `InventoryManagementSystem` composes a collection of `Product` objects.

3. **Inheritance:**
   - Inheritance is used to create domain-specific classes (`Book` and `Product`) derived from the `Entity` base class.
   - Derived classes inherit common attributes and methods from the base class and extend functionality with domain-specific features.
   - The `LibraryManagementSystem` and `InventoryManagementSystem` classes inherit from the generic `ManagementSystem` template class.

### Conclusion:

The project demonstrates the effective use of object-oriented programming principles, including overloading, composition, and inheritance, to design a modular and extensible management system. The command-line interface provides a user-friendly way to interact with the systems, and the design allows for easy adaptation to new domains or additional functionalities. The flexibility of templates and the reusability of code contribute to a scalable and maintainable solution.
