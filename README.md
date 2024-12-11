
# Coffee Orders Project


## Problem Statement

This report shows an analysis of Coffee Sales shop to draw business insights  by providing realtime insights from sales spreading over three countries . It helps the shop to monitor and analyze critical metrics related to top customers ,sales by country, and trending of sales as per each coffee type. 

## Objectives
- Tracking of top customers
- Best Sales by Country
- Trending Sales Analysis(Catergorized by coffee type)




### Steps followed 

- Step 1 : Load data into Excel Worksheet, dataset is a csv file.Data has seperate tables which need to be combined
- Step 2 : Joining of the orders table with customer table using XLOOKUP
a) Joining orders table to customer through customer ID

       =XLOOKUP(C2,customers!$A$2:$A$1001,customers!$B$2:$B$1001,,0)

       =IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0))

       =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)

b) Joining of the orders table to the product table using XLOOKUP, INDEX And MATCH

     INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))


- Step 3 : Performed data cleaning techniques
          a) Check and corrected data types accross all columns
          b) Trimmed all spaces in all columns 
          c) Wrote in full abbreviations such as Coffee type R = Robusta using IF Statements

          IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica"))))


          =IF(J2="M","Medium",IF(J2="L","Light",IF(J2="D","Dark")))
          
          d) Performed data formatting into short date format.
- Step 4 : Added a Sales column by using multiplication of quantity colun and unit price

        
- Step 5 : In the pivot tables worksheet, the first pivot table and chart inserted based on top five customers based on revenue they generated.
      
   ![Screenshot 2024-12-11 165337](https://github.com/user-attachments/assets/022e9933-eab1-4c51-ac85-b5204b67f59d)

  

- Step 6 : The second pivot table worksheet was based coffee sales by country.

![Screenshot 2024-12-11 165900](https://github.com/user-attachments/assets/056b79fc-5bcd-4f38-b37e-4f44618664cb)



- Step 7 : The third pivot table and chart was based on the trending over time analysis of each type of coffee. 


![Screenshot 2024-12-11 170418](https://github.com/user-attachments/assets/389befdf-de63-42f8-9a3b-6f124f0a2da4)


- Step 8 : Into the dashboard worksheet,
3 slicers based upon 
                     a) Coffee Roast Type
                     b) Size
                     c) Loyalty Card
                      were inserted for filtering.

![Screenshot 2024-12-11 170641](https://github.com/user-attachments/assets/1fc4f526-f029-4bbb-aefc-00dc1eb2b9c7)


 
- Step 9 : The pivot tables were combined to comeup with a dashboard 

 
![Screenshot 2024-12-11 170817](https://github.com/user-attachments/assets/7fc20984-6573-4327-91ab-fae14e270f65)



# Insights

A single page dashboard was created on Ms Excel.

Following insights can be drawn from the dashboard;


       a) United States generated most coffee sales amounting to $35 639
       b) Allis Willmore is the top performing customer with revenue genrated to $ 317
       c) Arabica Coffee type generated the most sales through the period.
       
       

           

 

