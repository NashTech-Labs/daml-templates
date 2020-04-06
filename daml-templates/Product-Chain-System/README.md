# DAML_CRUD-

## Following example shows Tri-party contract between
 1: Manufacturer
 2: Distributor / Wholesaler
 3: Consumer

There are two possible cases where manufacturer provides his service to wholesaler.
By providing a jobwork facility to wholesaler where wholesaler come with request of producing a particular product with definite quantity.
By producing their own product and making a proposal to wholesaler.


 With production of any product a ownership tag is attached with it so in case of jobwork product is produced by manufacturer but ownership of product is held to Client. While in cases where the manufacturer produces their own product ownership lies to the manufacturer.

## Compile
Create dar file using
```bash
daml build
```
Generate scala code of templates using
```bash
daml codegen scala
```
Finally start the sandbox with the dar file created at first step
```bash
daml sandbox ./.daml/dist/quickstart-0.0.1.dar
```

## Scenarios covered

Case where manufacture goes to wholesaler and wholesaler accepts the product then ownership transfer from manufacturer to wholesaler.

Case where manufacturer produces product on the request of client in such case client is owner from beginning.

## Scenario execution
Run test scenarios using 
```bash
daml damlc -- test --files Main.daml
```
