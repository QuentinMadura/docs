# DISPLAY.LIKE, DISPLAYLIKE

<PageHeader />

The **DISPLAY.LIKE** keyword is used to indicate that a field is to be displayed using the attributes of another field defined in the same dictionary.

## Syntax

```
field.name DISPLAY.LIKE alt.field
```

where:

**field.name** is the field name or EVAL expression to be displayed.  
**alt.field** is the field from which the attributes are to be derived when **field.name** is displayed.

## Example

```
LIST BOOK_SALES EVAL "FORENAME : ' ' : SURNAME" AS FULLNAME DISPLAY.LIKE SURNAME
```

Back to [Cross Reference](./../README.md)

<PageFooter />
