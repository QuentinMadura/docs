# FILEINFO

<PageHeader />

**Tags:**
<badge text='file operations' vertical='middle' />

## Description

Use the **FILEINFO** function to return information about the specified file variable. It takes the general form:

```
FILEINFO(file.variable, key)
```

This function is currently limited to return values to determine if the file variable is a valid file descriptor.

**Key** returns 1 if **file.variable** is a valid files variable, or 0 if not.

```
OPEN "test_rec" TO file_Var ELSE ABORT 201, "This file "
IF FILEINFO(file_Var, 0) = 1 THEN CRT "File information is valid"
ELSE
    CRT "Invalid information"
END
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
