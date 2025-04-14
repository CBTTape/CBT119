# CBT119
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 119 IS FROM MR HOWARD DEAN, FORMERLY OF SYNTEX, AND       *   FILE 119
//*           CONTAINS SEVERAL OF THEIR UTILITIES AND PROGRAMS.     *   FILE 119
//*                                                                 *   FILE 119
//*       Further support:  Sam Golob                               *   FILE 119
//*                 email:  sbgolob@cbttape.org                     *   FILE 119
//*                                                                 *   FILE 119
//*       Please note that File 136, also from Howard Dean, is      *   FILE 119
//*       of a later date than this file, so File 136 should        *   FILE 119
//*       also be consulted before installing anything from         *   FILE 119
//*       this file, just to check that there isn't something       *   FILE 119
//*       newer.  (SG)                                              *   FILE 119
//*                                                                 *   FILE 119
//*       Members in this file which have corresponding members     *   FILE 119
//*       in CBT File 136 are:                                      *   FILE 119
//*                                                                 *   FILE 119
//*       APUT ASID CPPL CSPL EPUTL EPUTL$ EPUTLO HMDCHRON          *   FILE 119
//*       HTIME INUSE IOPL JULGREG LDROP LUSE PDFINIT REGS          *   FILE 119
//*       TSOENTER TSOLEAVE XABSM                                   *   FILE 119
//*                                                                 *   FILE 119
//*           ==================================================    *   FILE 119
//*                       STARTED TASK ACCOUNTING AND               *   FILE 119
//*                       JES2 CONTROL CARDS IN STARTED             *   FILE 119
//*                       TASKS                                     *   FILE 119
//*           ==================================================    *   FILE 119
//*           JOBNAME     FRONT END TO 'STARTED TASK                *   FILE 119
//*                       CONTROL' FOR ADDING JOB                   *   FILE 119
//*                       ACCOUNTING AND JES2 CONTROL CARDS         *   FILE 119
//*                       * THIS CODE IS ON FILE 426 OF THE         *   FILE 119
//*                       CBT MODS TAPE *                           *   FILE 119
//*           LM00038     PART 1 LOCAL MODIFICATION FOR             *   FILE 119
//*                       STARTED TASK ACCOUNTING                   *   FILE 119
//*           LM00039     PART 2 LOCAL MODIFICATION FOR             *   FILE 119
//*                       STARTED TASK ACCOUNTING                   *   FILE 119
//*           STCADOC     FORMAT OF 'SYS3.STCACCT' MEMBERS          *   FILE 119
//*           X1          EXAMPLE OF STC ACCOUNTING (STARTS)        *   FILE 119
//*           ==================================================    *   FILE 119
//*                       IEFDB401 AND JES2 USER EXIT 6             *   FILE 119
//*           ==================================================    *   FILE 119
//*           DYNANAME    SAMPLE DYNAMIC UNIT NAME INPUT            *   FILE 119
//*                       FOR DYNAMASK                              *   FILE 119
//*           DYNAJOB     DYNAMASK CATALOGED PROCEDURE              *   FILE 119
//*           IEFDB401    DYNAMIC ALLOCATION EXIT TO                *   FILE 119
//*                       SUPPORT DYNAMIC UNIT NAMES                *   FILE 119
//*           JESUX006    JES2 USER EXIT TO SUPPORT DYNAMIC         *   FILE 119
//*                       UNIT NAMES                                *   FILE 119
//*           UNITDOC     DOCUMENTATION AND JUSTIFICATION           *   FILE 119
//*                       FOR DYNAMIC UNIT NAME                     *   FILE 119
//*                       MODIFICATION.                             *   FILE 119
//*           ==================================================    *   FILE 119
//*                       DUMP TRANSFER UTILITY                     *   FILE 119
//*           ==================================================    *   FILE 119
//*           B           CLIST FOR INVOKING ISPF BROWSE            *   FILE 119
//*                       FROM EITHER READY MODE OR AN ISPF         *   FILE 119
//*                       ENVIRONMENT.                              *   FILE 119
//*           E           CLIST FOR INVOKING ISPF 'EDIT'            *   FILE 119
//*                       FROM EITHER READY MODE OR AN ISPF         *   FILE 119
//*                       ENVIRONMENT                               *   FILE 119
//*           JULDATE     INNER CLIST FOR EXTRACTING                *   FILE 119
//*                       TIME/DATE/DAY OF WEEK                     *   FILE 119
//*                       ===>   (THIS CLIST CAN BE USED AS         *   FILE 119
//*                       A GENERAL DATE ROUTINE)                   *   FILE 119
//*           MAKEDAY     CLIST TO INITIALIZE DUMP TRANSFER         *   FILE 119
//*                       PDS                                       *   FILE 119
//*           XFERJOB     JOB TO TRANSFER SYSTEM DUMP               *   FILE 119
//*                       DATASET TO TAPE                           *   FILE 119
//*           XFERINST    HINTS ON INSTALLATION OF THE DUMP         *   FILE 119
//*                       TRANSFER UTILITY                          *   FILE 119
//*           XFERUTIL    TSO COMMAND SUBROUTINE TO                 *   FILE 119
//*                       DETERMINE DUMP DATASET VOLUME             *   FILE 119
//*                       SERIAL.                                   *   FILE 119
//*           XFERVOL     SUBROUTINE OF XFERUTIL TO                 *   FILE 119
//*                       DETERMINE VOLUME SERIAL #                 *   FILE 119
//*           XFERWTO     PROGRAM TO ISSUE WTO FROM SYSIN           *   FILE 119
//*                       (USED WITH CLISTS)                        *   FILE 119
//*           XFER1       CLIST INVOKED UNDER TMP IN BATCH          *   FILE 119
//*                       TO UPDATE XFER PDS                        *   FILE 119
//*           XFER2       CLIST INVOKED UNDER TMP IN BATCH          *   FILE 119
//*                       TO UPDATE XFER PDS                        *   FILE 119
//*           XIX         CLIST TO INQUIRE INTO THE DUMP            *   FILE 119
//*                       TITLE DATABASE                            *   FILE 119
//*           XIXHELP     HELP MEMBER FOR XIX CLIST                 *   FILE 119
//*           ==================================================    *   FILE 119
//*                       TSO COMMANDS AND UTILITIES                *   FILE 119
//*           ==================================================    *   FILE 119
//*           ASID        COMMAND TO PRINT ADDRESS SPACE            *   FILE 119
//*                       DATA CONVERTED TO WORK IN 31 BIT          *   FILE 119
//*                       MODE UNDER MVS/XA (WORKS ON               *   FILE 119
//*                       NON-XA SYSTEMS TOO, IF VARIABLE           *   FILE 119
//*                       SET)                                      *   FILE 119
//*           ASHELP      HELP TEXT FOR THE 'ASID' COMMAND          *   FILE 119
//*           CLR3270     COMMAND TO CLEAR SCREEN OF 3270           *   FILE 119
//*                       TERMINAL. CHECKS FOR SESSION              *   FILE 119
//*                       MANAGER ACTIVE AND RETURNS NULL           *   FILE 119
//*                       STRING TO AVOID FLICKER.                  *   FILE 119
//*                       (Fixed by William Smith to work           *   FILE 119
//*                       properly under more adverse conditions.)  *   FILE 119
//*           CLRHELP     HELP TEXT FOR THE 'CLR3270'               *   FILE 119
//*                       COMMAND                                   *   FILE 119
//*           HMDCHRON    TIME OF DAY UTILITY - CONVERT             *   FILE 119
//*                       TIME-OF-DAY                               *   FILE 119
//*           JULGREG     JULIAN-GREGORIAN AND VICE-VERSA           *   FILE 119
//*                       CONVERSION (SUBROUTINE OF                 *   FILE 119
//*                       HMDCHRON)                                 *   FILE 119
//*           HTIME       TSO COMMAND TO FORMAT THE DATE            *   FILE 119
//*                       AND TIME OF DAY (CALLS HMDCHRON           *   FILE 119
//*                       AS SUBROUTINE)                            *   FILE 119
//*           PDFINIT     PROGRAM FOR ALLOCATING THE "ISPF"         *   FILE 119
//*                       PROFILE DATASET AND OPTIONALLY            *   FILE 119
//*                       INVOKING EITHER A COMMAND OR              *   FILE 119
//*                       "USERID.PROFILE.CLIST" UPON               *   FILE 119
//*                       LOGON. CAN BE SET UP SIMILIAR TO          *   FILE 119
//*                       VM PROFILE EXEC INVOCATION.               *   FILE 119
//*           PDFHELP     HELP TEXT FOR THE 'PDFINIT'               *   FILE 119
//*                       COMMAND                                   *   FILE 119
//*           SM          COMMAND TO TURN SESSION MANAGER           *   FILE 119
//*                       ON/OFF. WORKS IN MVX/XA MODE              *   FILE 119
//*                       WHERE SESSION MANAGER CONTROL             *   FILE 119
//*                       BLOCKS ARE MOVED 'ABOVE THE               *   FILE 119
//*                       LINE'.  (SM tested to run on z/OS 2.2. )  *   FILE 119
//*           ==================================================    *   FILE 119
//*                       MACROS AND SUBROUTINES                    *   FILE 119
//*           ==================================================    *   FILE 119
//*           EPUTL       PUTLINE SUBROUTINE TO ACCEPT PARM         *   FILE 119
//*                       LIST "ABOVE THE LINE"                     *   FILE 119
//*                       (Cleaned up a bit by Sam Golob)           *   FILE 119
//*           APUT        MACRO TO INVOKE 'EPUTL' INSTEAD           *   FILE 119
//*                       OF TPUT                                   *   FILE 119
//*           --------------------------------------------------    *   FILE 119
//*           CALL#       INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           DATA#       INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           END#        INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           ENDDATA#    INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           ENTRE#      INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           EXIT#       INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           IEXIT#      INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           INIT#       INTERNAL STRUCTURED MACROS USED           *   FILE 119
//*                       BY XFER UTILITY                           *   FILE 119
//*           --------------------------------------------------    *   FILE 119
//*           INUSE       INNER MACRO FOR                           *   FILE 119
//*                       TSOENTER/TSOLEAVE/SETREG/EOJ              *   FILE 119
//*           LUSE        INNER MACRO FOR                           *   FILE 119
//*                       TSOENTER/TSOLEAVE/SETREG/EOJ              *   FILE 119
//*           LDROP       INNER MACRO FOR                           *   FILE 119
//*                       TSOENTER/TSOLEAVE/SETREG/EOJ              *   FILE 119
//*           CSPL        INNER MACRO FOR TSOENTER/TSOLEAVE         *   FILE 119
//*           IOPL        INNER MACRO FOR TSOENTER/TSOLEAVE         *   FILE 119
//*           CPPL        INNER MACRO FOR TSOENTER/TSOLEAVE         *   FILE 119
//*           TSOENTER    MACRO TO SET UP COMMAND PROCESSOR         *   FILE 119
//*                       ENVIRONMENT                               *   FILE 119
//*           TSOLEAVE    MACRO TO RETURN TO TMP (USED              *   FILE 119
//*                       W/TSOENTER)                               *   FILE 119
//*           SETREG      ENTRY SETUP MACRO  - NON/TSO              *   FILE 119
//*                       ENVIRONMENT                               *   FILE 119
//*           EOJ         EXIT  RETURN MACRO - NON/TSO              *   FILE 119
//*                       ENVIRONMENT                               *   FILE 119
//*           XABSM       BRANCH AND SET MODE MACRO FOR             *   FILE 119
//*                       MVS/XA 31 BIT CODING                      *   FILE 119
//*                                                                 *   FILE 119
```
