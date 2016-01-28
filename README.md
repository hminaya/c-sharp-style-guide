# C# Style Guide
Just trying to setup some simple guides, not trying to conquer the world.

## Nomenclature

#### Namespaces
abc
#### Classes
abc
#### Functions
abc

## Migrations (based on [Fluent Migrations](https://github.com/schambers/fluentmigrator))

#### Unique Identifiers
All migrations are based on an Unique identifier. A Timestamp that includes the year, month, day, hour and minute. Example:

```c#
201601290937
```
Translates to:
* 2016 - year
* 01 - month
* 29 - day
* 09 - hour
* 37 - minute

This isn't a fool proof method, but provides a good starting point for most teams.

#### Filenames
These should be ordered by a datestamp and should describe what is being done without having to look through the source code.

__Adding Columns__
* Adding a column named *first_name* to a table called *profile*

```c#
201601290937_add_first_name_to_profile.cs
```

__Adding Multiple Columns__
* Adding two columns, one named *first_name* and the other *last_name* to a table called *profile*

```c#
201601290937_add_first_name_and_last_name_to_profile.cs
```

#### Class names
Classes should use __CapitalizedCamelCase__ for their names

```c#
public ...
```

#### Data Annotations, Table and Column mappings
If the DB you are working with does not follow any modern naming conventions (which happens a lot in Legacy systems), then all classes should be mapped with the corresponding data annotation attribute to their exact table name. Thus preserving EF coding guidelines and conventions. The same goes for column names.

```c#
public ...
```
