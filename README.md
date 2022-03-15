# Excel_Formulas
A reference list of my frequently used Excel Formulas used in my daily work

## Index Match 
This was my first time working with Index Match and had been pretty handy.  However, this formula is not code efficient and can cause overflow problems.   
1. =IF(ISNA(INDEX(A:A, MATCH(B:B, I:I, 0))), "", IF(INDEX(A:A, MATCH(B:B, I:I, 0))=0, "", INDEX(A:A, MATCH(B:B, I:I, 0))))    

My revised version that works more efficiently for my data sets!    
2. =INDEX(B:B,MATCH(C2,A:A,0))   

After working for a long time, I finally needed an index match formula that required meeting 2 search criteria.  The 5, represents the data column that will populate from the array.   
3.    =INDEX(code!A:G,MATCH(1,(B82=code!A:A)*(P82=code!G:G),0),5)   


Key Sources:    
https://spreadsheeto.com/index-match/     
https://www.contextures.com/excellookupmultiplecriteriaindexmatch.html#matchmulti    
https://stackoverflow.com/questions/26373325/if-two-cells-match-return-value-from-third/26373415     

## Comparing Lists
=IF(ISNUMBER(MATCH(  ,  ,0)),"Yes","No")   

=IF(ISNUMBER(MATCH(A2,Courses!B:B,0)),"Yes","No")     

Put the lookup cell in the first blank spot and the lookup array in the second blank spot to compare a list quickly.

## Alternating banded rows based on one matching input
https://www.redargyle.com/blog/alternate-row-color-based-value-change-google-sheets/

------------------   
Data Scientist Roadmap
https://github.com/MrMimic/data-scientist-roadmap
https://github.com/visenger/awesome-mlops
https://www.linkedin.com/pulse/free-data-science-books-20-steve-nouri/
