# Data Modeling :
        It is method of organizing the data by connecting dim tabels with facts tabels which can be analyzed easily.

-> Advantages of data modeling :
    * Easy to write DAX quries [filter can be easily controlled one to many]
    * Easy to implement RLS 
    * Easy to understand


## Two types of Schemas:
 * Star Schema and show flake schema

* Start Schema : Multiple dimensions are connected to one fact table in some cases one fact table is connected to all dimensions

* Snowflake Schema : Multiple dimensions are connected to one fact table w.r.t dimension are connected to some other dimension table which is not connected to fact table.

## Model types :
**Conceptual Model** :   
                    ----------------
                    |    Category   |
                    ----------------
                            |
                           \ /
                    ----------------
                    |   Product   |
                    ----------------       
 **Logical Model** :   
                    ----------------------------
                    |    Category(Tabel name)   |
                    |    genderTyoe             |
                    |    size                   |
                    ----------------------------
                            |
                           \ /
                   -----------------------------
                    |   Product (Tabel name)    |
                    |   Quantity                |
                    |   colour                  |
                    -----------------------------      

**Physical Model**:   
                    ----------------------------
                    |    Category(Tabel name)   |
                    |    genderTyoe  (text)     |
                    |    size (num)              |
                    ----------------------------
                            |
                           \ /
                   -----------------------------
                    |   Product (Tabel name)    |
                    |   Quantity   (num)        |
                    |   colour    (text)        |
                    -----------------------------                   

### Dimensional Table:
    The Dim table describes about the data like product, customer, calender, store details 

### Fact tables:
    Transactional data/quantitative info 
* Structure of Fact table:
$$
first part [primary table]
second part[Dimensional SK keys]
Third part [fact table data]
$$




## Surrogative key:

 * The key used to uniquely identify the row
 * it satrts from 1 and increments by 1
 * Used in dim tables
 * No Primary key or forign key is to be used in Azure Warehouse.




