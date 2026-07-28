## Application Overview
This Zoho Creator app manages custom gate and shutter work from order entry through production, purchasing, permits, installation, service, inventory, and user administration. It includes role home pages, detail pages, queue actions, stock alerts, and admin-only user management.

## Forms
| Form Name | Purpose | Key Lookups |
|---|---|---|
| Unit_Master | Units | - |
| Add_Employee | Employee directory | Manager |
| Staff_Master | Legacy staff directory | - |
| Customer_Master | Customers | - |
| Vendor_Master | Vendors | - |
| Material_Master | Material stock | Unit, Vendor |
| Powder_Coating_Inventory | Powder stock | Vendor |
| Product_Catalogue | Products | Unit/Powder |
| Product_BOM_Items | BOM defaults | Product, Material |
| Customer_Orders | Order header | Customer |
| Order_Line_Items | Order lines/queues | Order, Product |
| Set_Queue_Position | Queue update form | Order line |
| Manufacturing_Groups | Production batches | Orders/Staff |
| Production_Records | Build tracking | Order line, Group |
| Production_Material_Usage | Material use | Production, Material |
| Purchase_Orders | PO header | Vendor |
| Purchase_Order_Lines | PO lines | PO, item |
| Installation_Schedules | Install planning | Order, Staff |
| Permit_Records | Permit tracking | Order/Customer |
| Service_Requests | Service tickets | Customer, Order, Staff |
| Service_Parts_Usage | Service stock use | Service, Material |
| Action_Comments | Activity notes | Related record |
| Add_Users | User admin | Profile |

## Reports
| Report Name | Type | Source Form |
|---|---|---|
| Master reports; All_Employees; Active_Field_Employees | List | Master forms |
| Order reports and delivery calendar | List/Calendar | Orders, lines |
| Production reports; Production_Queue | List/Spreadsheet/Kanban | Lines, production |
| Purchase reports and receiving calendar | List/Calendar | POs, PO lines |
| Installation reports; Installation_Queue | List/Calendar/Kanban | Lines, installs |
| Permit reports and expiry calendar | List/Calendar | Permit_Records |
| Service reports/calendar/board | List/Calendar/Kanban | Service forms |
| All_Action_Comments; All_Users | List | Notes, users |

## Pages
| Page Name | Purpose | Key Components |
|---|---|---|
| Role home pages | Dashboards by role | HTML snippets, KPIs, tables |
| Detail pages | Record drilldowns | Snippets, badges, timelines |

## Design Decisions
- Add_Employee is the visible employee master; Staff_Master remains for legacy links.
- Production_Queue and Installation_Queue expose queue-number actions from line reports.
- Add_Users is mapped but hidden from everyday navigation and admin-controlled.
- Every surfaced report has a web DeviceUI quickview/detailview layout.