# utl-ingenious-technique-to-map-F-D-A-to-1-2-3
Ingenious technique to map F D A to 1 2 3
    Ingenious technique to map F D A to 1 2 3

    To simple to post?

    Problem

       F = 1
       D = 2
       A = 3


    Related to

    SAS Forum
    https://tinyurl.com/y9rnjn9d
    https://communities.sas.com/t5/New-SAS-User/How-do-I-add-a-column-to-a-dataset-that-stores-categories-from/m-p/516178


    PROCESS
    =======

    data want;

      do ltr='D','A','F';
         decode=index('FDA',ltr);
         put decode=;
         output;
      end;

    run;quit;

    OUTPUT
    ======

     WORK.WANT total obs=3

      LTR    DECODE

       D        2
       A        3
       F        1


