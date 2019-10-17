## Autumn Raven Crafts

This is a snippet of SQL designed to create a couple of tables in a database for a small crafting business that makes custom vinyl prints
adheres them to t-shirts, bags, or used as decals on vehicles. One of the tables is used to keep inventory of available vinyls in different
colors and transfer types.  The other table is for storing customer information.



```SQL

CREATE DATABASE AutumnRavenCrafts;

CREATE TABLE IF NOT EXISTS `AutumnRavenCrafts`.`Inventory` (
  `InventoryID` INT NOT NULL,
  `VinylType` VARCHAR(45) NULL,
  `VinylColor` VARCHAR(45) NULL,
  `SheetCount` INT NULL,
  `PartialSheetCount` INT NULL,
  PRIMARY KEY (`InventoryID`),
  UNIQUE INDEX `InventoryID_UNIQUE` (`InventoryID` ASC) VISIBLE);
  
CREATE TABLE IF NOT EXISTS `AutumnRavenCrafts`.`Customer` (
  `idCustomer` INT NOT NULL,
  `Name` VARCHAR(45) NULL,
  `Address` VARCHAR(45) NULL,
  `City` VARCHAR(45) NULL,
  `State` VARCHAR(45) NULL,
  `Zip` VARCHAR(45) NULL,
  `Email` VARCHAR(45) NULL,
  `PhoneNumber` VARCHAR(10) NULL,
  PRIMARY KEY (`idCustomer`));
  
```
