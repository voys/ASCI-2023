**Puzzle 2: Locked out**:

You arrive at the Voys office in het Kwadraat early in the morning, ready to tackle the day. However, upon reaching the front door, you find yourself unable to enter. The company's state-of-the-art security system, which uses a certain password protocol, appears to have locked out all employees.

A small note attached to the door reads, "System locked due to password discrepancies. Access denied until verification can be performed." With a sigh, you realize it's going to be one of those days.

You open up Slack and ask within the security channel what's going on. They explain the situation: during a routine upgrade, a script that was supposed to hash and re-encrypt passwords had a bug, leaving the password validation system in disarray. They've been locked out as well until all passwords are verified.

As the security team's last hope, they provide you with a list _(your puzzle input)_ of employee passwords according to the database, alongside the official password policy in place at the time of their creation.

For example, they send you a snippet that looks like this:

```
3-6 e: leurrtgbeeur
5-6 h: pshafhxhhhch
3-6 l: lcpoqlwklpco
```

Each line represents an employee's password record. The password policy indicates the minimum and maximum number of times a specific character must appear for the password to be valid. As per the policy `3-6 e` the password must contain the character 'e' at least three and at most six times.

In the above example:

- `3-6 e: leurrtgbeeur` is valid since the letter `e` can be found 3 times.
- `5-6 h: pshhfhxhhhch` is invalid since the letter `h` can be found 7 times.
- `4-6 l: llpoqlwklpco` is valid since the letter `l` can be found 3 times.

The security team needs to know which passwords would have been valid according to the official policy so that they can reset those that are non-compliant and restore system access.

Out of the snippet provided, the task is to assess the passwords listed and determine how many are valid according to the policy so you and everyone else can gain entry and start your day at Voys.

_**How many passwords in the list are valid according to the security policy?**_
