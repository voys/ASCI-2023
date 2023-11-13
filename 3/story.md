**Puzzle 3: Voys Welcome Kits Mishap**

At Voys the deployment team faced an unexpected challenge. It was discovered that during the packaging of the new customer welcome kits, which included hardware devices like VoIP phones and access to Voys' proprietary software, a critical error had occurred.

The welcome kits were Voys' boxes designed with two compartments: one for the physical telephony devices such as headsets, VoIP phones, and adapters (compartment "Hardware"), and the other for the software elements like mobile apps, webphone credentials, and codecs (compartment "Software").

Each item was to be uniquely identified by a letter code: uppercase for hardware components and lowercase for software components. Due to a programming error in the automated packing script, one type of software component was mistakenly placed in both compartments of each rucksack.

Voys' engineers quickly put together an inventory report of the packed boxes. They're now enlisting your expertise to create a program that can spot these discrepancies.

Here's a snapshot of the inventory for six boxes as an example:

```
vJrwpWtwJgWrhcsFMMfFFhFp
jqHRNqRjqzjGDLGLrsFMfFZSrLrFZsSL
PmmdzqPrVvPwwTWBwg
wMqvLMZHhHMvwLHjbvcjnnSBnvTQFn
ttgJtRGJQctTZtZT
CrZsJsPPZsGzwwsLwLmpwMDw
```

- The first box contains the items vJrwpWtwJgWrhcsFMMfFFhFp, which means its first compartment contains the items vJrwpWtwJgWr, while the second compartment contains the items hcsFMMfFFhFp. The only item type that appears in both compartments is lowercase p.
- The second box's compartments contain jqHRNqRjqzjGDLGL and rsFMfFZSrLrFZsSL. The only item type that appears in both compartments is uppercase L.
- The third box's compartments contain PmmdzqPrV and vPwwTWBwg; the only common item type is uppercase P.
- The fourth box's compartments only share item type v.
- The fifth box's compartments only share item type t.
- The sixth box's compartments only share item type s.

To help prioritize item rearrangement, every item type can be converted to a priority:

- Lowercase letters (software components) are assigned priorities from 1 to 26, corresponding to 'a' through 'z'.
- Uppercase letters (hardware components) are assigned priorities from 27 to 52, corresponding to 'A' through 'Z'.

In the above example, the priority of the item type that appears in both compartments of each box is 16 (p), 38 (L), 42 (P), 22 (v), 20 (t), and 19 (s); the sum of these is 157.

Find the item type that appears in both compartments of each box. What is the sum of the priorities of those item types?

_**What is the sum of the priorities of those item types?**_
