**Puzzle 4: The Voys Blockchain**

At Voys, we are developing our own blockchain. The difference with other blockchain technologies is that not computers, but employees approve transactions. Before a transaction is approved, it must pass through all employees according to a fixed pattern.

This pattern is represented in a list of dependencies. For each line, it states what is needed for the next employee.

Take, for example, this list:

```
Timon must be ready before Anton can start checking.
Timon must be ready before Pascal can start checking.
Anton must be ready before Esther can start checking.
Anton must be ready before Dagmar can start checking.
Esther must be ready before Mark can start checking.
Dagmar must be ready before Mark can start checking.
Pascal must be ready before Mark can start checking.
```

Visually, the dependencies look like this:

```
  -->Anton---->Esther
 /    \         \
Timon  Dagmar----->Mark
 \              /
  -------->Pascal
```

Your task is to determine the correct order of steps. If more than one step can be taken, choose the step that comes first in alphabetical order.

In the example, this becomes:
- Only `Timon` can start checking because he has no dependencies.
- Then `Anton` and `Pascal` can start checking. The `A` comes first in the alphabet, so `Anton` goes first.
- Although `Pascal` was available earlier, `Esther` and `Dagmar` are now also available. The `D` comes before `E` and `P` in the alphabet, so `Dagmar` goes now.
- Next, only `Esther` and `Pascal` are available. `Mark` is not yet available because not all of `Mark`'s dependencies have been met. Therefore, `Esther` is now up.
- `Pascal` is the only choice available now.
- Finally, it's `Mark`'s turn.

So in this example, the correct order is: `Timon, Anton, Dagmar, Esther, Pascal, Mark`.

_**What is the correct order of steps given the input?**_
