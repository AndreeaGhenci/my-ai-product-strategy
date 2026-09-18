# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | GhitHub| H | This month: Review if the product can be moved onto another platform quickly.|
| **Abstraction** | ADO| M | This quarter: Review if there is there is hard-coding of vendor and/or models.|
| **Routing** | No dynamic routing depending on model, vendor, latency etc| H | This Quarter: Prioritize implementation of dynamic routing based on cost and latency.|
| **Eval** | Testing is not automated meaning that any switch in vendor would need to be tested manually, putting the 48 hour switch at risk | H | This quarter: Prioritize and implement automated testing.|

## Portability Score
<!-- Ready / Partial / Locked --> Partial 

## If [primary vendor] doubles pricing tomorrow: GhitHub/ ADO
<!-- What's your 48-hour response? --> Major fail. Would have to pay the money.

## If [primary vendor] ships a competing product: GitHub/ ADO
<!-- What's defensible that they can't replicate? --> They don't actually have the data. 
