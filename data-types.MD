YAML supports various data types to represent different kinds of information, and it also allows the use of multiple documents within a single YAML file. Here’s a detailed overview:

### YAML Data Types

1. **Scalars**

   Scalars are the basic data types that hold simple values. YAML supports several types of scalars:

   - **String**: Represents text. Can be written in plain style, double-quoted, or single-quoted.

     ```yaml
     plain_string: Hello, World!
     double_quoted_string: "This is a string with special characters like \n and \"quotes\"."
     single_quoted_string: 'This is a string with a single quote (\') and \n is just text.'
     ```

   - **Integer**: Represents whole numbers.

     ```yaml
     age: 30
     ```

   - **Floating Point**: Represents decimal numbers.

     ```yaml
     price: 19.99
     ```

   - **Boolean**: Represents `true` or `false`.

     ```yaml
     is_active: true
     is_verified: false
     ```

   - **Null**: Represents a null value. Can be represented as `null`, `~`, or simply an empty value.

     ```yaml
     value1: null
     value2: ~
     value3: 
     ```

2. **Collections**

   - **List (Array)**: Represents an ordered collection of items. Each item is prefixed with a dash.

     ```yaml
     fruits:
       - Apple
       - Banana
       - Orange
     ```

   - **Dictionary (Map)**: Represents an unordered collection of key-value pairs.

     ```yaml
     person:
       name: John Doe
       age: 30
     ```

   - **Nested Lists and Dictionaries**: Lists and dictionaries can be nested inside each other.

     ```yaml
     complex_structure:
       - name: Alice
         age: 28
         interests:
           - Reading
           - Hiking
       - name: Bob
         age: 35
         interests:
           - Cooking
           - Traveling
     ```

3. **Complex Data Types**

   - **Date**: Represents a date in `YYYY-MM-DD` format.

     ```yaml
     birth_date: 1994-05-14
     ```

   - **Timestamp**: Represents date and time in `YYYY-MM-DDTHH:MM:SSZ` format.

     ```yaml
     created_at: 2024-09-19T12:34:56Z
     ```

   - **Custom Types**: YAML allows custom data types using tags. Tags are usually defined with `!`.

     ```yaml
     !my_custom_type
     data: value
     ```

### Multiple Documents in YAML

YAML supports multiple documents within a single file, separated by `---`. This is useful for defining multiple configurations or datasets in a single file.

```yaml
# First document
application:
  name: MyApp
  version: 1.0.0

---

# Second document
database:
  host: db.example.com
  port: 5432

---

# Third document
logging:
  level: info
  file: /var/log/myapp.log
```

In this example, each document is separated by `---`, and you can include any number of documents in a single YAML file.

### Summary

YAML data types include:

- **Scalars**: Strings, integers, floating-point numbers, booleans, and null values.
- **Collections**: Lists (arrays) and dictionaries (maps).
- **Complex Types**: Dates, timestamps, and custom types.

Multiple documents in a YAML file are separated by `---`, allowing for flexible and organized data representation.
