# Library Catalog System

This Python project is a Library Catalog System that allows you to manage the catalog of a library, including items such as books, DVDs, and magazines.

## Table of Contents
- [Background](#background)
- [Requirements](#requirements)
- [Usage](#usage)
- [Class Hierarchy](#class-hierarchy)
- [Example Usage](#example-usage)
- [Contributing](#contributing)
- [License](#license)

## Background

You are tasked with developing a Python program to manage the catalog system of a library. The library contains various types of items such as books, DVDs, and magazines. Each item has unique attributes, and the library needs a system to check items in and out, as well as display information about the items in the catalog.

## Requirements

- Create a Python class hierarchy for the library catalog system.
- Implement a base class called `LibraryItem` with attributes for title, item ID, and availability.
- Create subclasses for different types of library items such as books and DVDs.
- Implement methods for checking items in and out, and displaying item information.
- Keep track of the total number of items in the library using class variables and methods.
- Ensure proper error handling for cases where an item is already checked out or does not exist in the catalog.

## Usage

To use this Library Catalog System, you can follow these steps:

1. Create instances of library items such as books, DVDs, or magazines.
2. Use the `checkout` and `return_item` methods to manage item availability.
3. Display item information using the `get_details` method.
4. Use the `items_present` class method to check the total number of items in the library.

## Class Hierarchy

- `LibraryItem` (Base Class)
  - Subclasses:
    - `book`
    - `DVD`
    - `magazine`

## Example Usage

Here's an example of how to use this Library Catalog System:

```python
# Create library items
book1 = book("The Catcher in the Rye", 'B1', "J.D. Salinger", "978-0-316-76948-0")
dvd1 = DVD("Inception", 'D1', "Christopher Nolan", 148)
magazine1 = magazine("National Geographic", 'MG1', "National Geographic Society", "September")

# Check out an item
book1.checkout()

# Return an item
book1.return_item()

# Display the total number of items in the library
total_items = LibraryItem.items_present()
print(f"Total items in the library: {total_items}")
