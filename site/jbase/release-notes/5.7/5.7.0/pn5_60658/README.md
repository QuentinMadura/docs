# PN5_60658

<PageHeader />

## Description

jQL: I-type dictionaries do not recognize @TM

### Previous Release Behavior

Previously, the following would fail:

```
    FULLADDR
001 I Both lines of address
002 IF ADDR2 THEN ADDR1:@TM:ADDR2 ELSE ADDR1
003
004 Street Address
005 30T

jsh home ~ -->LIST TESTFILE FULLADDR
Error in Statement "LIST TESTFILE FULLADDR"
Error in attribute definition item FULLADDR
Error in Itype: unexpected token: @TM
```

### Current Release Behavior

@TM is now recognized as a valid I-type token.

Note that although @TM will be recognised and work fine, as in the above example, there are no plans to extend MV processing to the @TM level. Currently there is @VM and limited @SM level processing only.

Also, the length specification in the I-type must accommodate the longest data to prevent the Text Mark from appearing in the data. A recommended method would be:

```
001 I
002 IF ADDR2 THEN ADDR1[1,30]:@TM:ADDR2[1,30] ELSE ADDR1
003
004
005 30T
```

Back to [jBASE 5.7.0 Release Notes](./../README.md)

<PageFooter />
