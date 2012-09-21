What's new in 2.2 ?

### Each type of column manage automaticaly array values.
The bundle detects the array type of the ORM annotation so you just have to define the type of the data of the array. 

Example:

```
    /*
     * @ORM\Column(type="array")
     *
     * @GRID\Column(type="number")
     */
    protected $my_numbers;
}
```

Note: Filters aren't completely done.

## Add Country, Language and Locale column with their select filter.
These new column are an extended TextColumn Class and the bundle detect the name of the property to add a specific instead of a TextColumn.
(country, countries, language, languages, locale, locales)

Example:

```
    /*
     * Automatic country column
     * @ORM\Column(type="string", length=2)
     */
    protected $country;
    
    /*
     * Automatic country column with array value support
     * @ORM\Column(type="array")
     */
    protected $countries;
    
    /*
     * Forced country column
     * @ORM\Column(type="string", length=2)
     * @GRID\Column(type="country")
     */
    protected $my_var;
}

## Add new operators

Doesn't start with
Doesn't end with
Not between exclusive
Not between inclusive
