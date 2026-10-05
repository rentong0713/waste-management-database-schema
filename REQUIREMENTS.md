## Business Requirements

**Clear Away** requires a centralized relational database to manage municipal waste collection logistics, track physical assets, and monitor local authority contracts.

The database must capture the following operational domains:

### 1. Geographic & Property Data

* Track **Local Authorities**, including:

  * CEO details
  * Total area
  * Classification: Borough, City, District Council, Shire, or Town
* Record **Street** logistics under each authority, including:

  * Road surface type: Asphalt, Concrete, or Unsealed
  * Street length
  * Number of lanes
* Map **properties to streets** and track **property ownership**, allowing multiple owners per property.

### 2. Contract & Waste Management

* Manage **waste collection contracts** signed with Local Authorities, including:

  * Contract start date
  * Contract end date
* Define **waste types**, such as General and Recycling.
* Track the **collection cost** and **collection frequency** for each waste type under specific contracts.

### 3. Asset Management (Bins)

* Maintain a **Bin Catalogue** detailing:

  * Available bin sizes
  * Standard supply costs for different waste types
* Track physical bins supplied to properties using **RFID tags**.
* Monitor the **bin lifecycle**, including:

  * Supply dates
  * Replacement reasons, such as Stolen, Bin Failure, or Damaged

### 4. Collection Logistics

* Register a fleet of **collection trucks**, tracking:

  * VIN
  * Make
  * Model
  * Year
* Schedule and record **Collection Runs** linked to:

  * Specific contracts
  * Waste types
  * Trucks
* Capture real-time collection metrics via **RFID**, including:

  * Total kilograms collected per bin
  * Whether the bin was flagged as overweight (`Y`/`N`)
