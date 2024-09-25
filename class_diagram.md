## Учет клиентов

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
```
## Учет материалов

```mermaid
classDiagram
    class MaterialAccounting {
        + string name
        + int quantity
    }
```

## Учет оборудования

```mermaid
classDiagram
    class EquipmentAccounting {
        + int accession_number
        + string specialist
        + string name
        + string status
        + string workshop
    }

```
## Учет сотрудников

```mermaid
classDiagram
    class EmployeeAccounting{
        + string full_name
        + string speciality
        + string status
        + string employee_number
    }