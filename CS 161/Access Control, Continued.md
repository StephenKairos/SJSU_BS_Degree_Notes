# Access Control, Continued

## Lampson's Access Control Matrix

* subjects (users): index rows
* columns: index columns
* r: read, w: write, x: execute
* permissions, basically
* ACL: store access control matrix by column, more likely to add new files than users, **usually used by OSes**
* C-List: capabilities, store by row

## Confused Deputy
* compiler and BILL file (billing info)
* compiler: w to file
* Alice: x to compiler, not w BILL
* compiler is deputy acting on behalf of Alice, confused rights between Alice and Compiler
* ACL is hard to avoid this issue
* solve by giving user list to deputy
* Capabilities are better for security, but ACLs are faster for OS, which is why ACL is still used

## Multilevel Secureity (MLS) Models
* classifications, apply to objects
* clearances apply to subjects
* Proper Classification not always clear
* Level of granularity to apply classifications
* aggregation- flipside of granularity
* **Notation**:
    * O: object, S: subject, L(X): level of X
* Network Firewall: keep intruder at low level to limit damage
* Models don't tell how to implement, descriptive, not prescriptive

## Bell-LaPadula
* confidentiality
* prevent unauthorized reading
* S can read O iff L(O) <= L(S)
* S can write O iff L(S) <= L(O)
* Completely prevent top secret douments from being disclosed
* **No read up, no write down**

## McLean's Criticisms and B/LP Response
* Too trivial
* Created "System Z", allows administator to reclassify object, then "write down"
* Tranquility Property:
    * Strong, used as is
    * Weak, allows changing of classification if within security policy
* "High Water Mark" principle

## Biba's Model
* integrity
* trust integrity of O1, bt not O2
    * if O3 includes O1 and O2, don't trust O3
* Low Watermark Principle
* So BLP for Read, Biba for Write
* S can write O iff L(O) <= L(S)
* S can read O iff
* L(S) <= L(O)

## Compartments
* Split levels into that may not contain each other
* Can be used without compartments
* MLS almost always uses compartments
* Example:
    * British Medical Association
    * AIDS was TOP SECRET, Prescriptions SECRET, with SECRET level, you could basically know what TOP SECRET levels are