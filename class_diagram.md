
`AccountingForOrders`
```mermaid
classDiagram
    class AClient {
        <<Abstract>>

        + string inn
        + string address
        + map~string, string~ contacts
    }

    AClient <|-- ClientYL
    class ClientYL {
        + string name
    }

    class AOrder {
        <<Abstract>>

       + sring number
       + string data
       + string comments
    }
    AOrder <|-- OrderItem
    OrderItem *-- ProductQuantity
    OrderItem *-- ClientYL
    class OrderItem {
       + string plann_date_of_execution
       + string fact_date of execution
       + vector<ProductQuantity> products

    }

    Product *-- ProductQuantity
    class Product {
       + string code
       + string names
       + doubl cost
 } 

    class ProductQuantity {
    + Product* product
    + int quantity
}

```
`ProductionOfProducts`
```mermaid
classDiagram
    class AStage {
        <<Abstract>>

        + string name
        + string time
    }

    AStage <|-- StageItem
    class StageItem {
        + string equipment
        + vector<pair<string, int>> materials
    }

    ProductionPlan *-- StageItem
    class ProductionPlan {
        + map<string, StageItem*> stages
    }
