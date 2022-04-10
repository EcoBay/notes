# Traditional File Processing (TFP)

In TFP every user defines and implements the needed files for a specific application to run.

<div class="mermaid">
graph LR;
    CO[Customer Orders]-->CF1[/Customer Files/] & SF1[/Stock File/] & OF1[/Order File/];
    CI[Customer Invoice]-->CF2[/Customer Files/] & SF2[/Stock File/] & OF2[/Order File/];
    PO[Purchase order]-->SF3[/Stock Files/] & SP1[/Supplier File/];
</div>

## Disadvantage

- Program-data dependence - when the program is destroyed data might be lost as it cannot be separated from the application
- Data redundancy - data might be stored multiple times in different application
- Limited data sharing - as applications store their own data.
- Lengthy Development Time - as they must also develop how each application store and retrieve data.
- Excessive Program Maintenance - As other than the application, files are also need to be maintained.
