**Puzzle 1: Helping out the Customer Success Circle**:

In the lead-up to the holiday rush, Voys is optimizing its customer support workflow.

The holidays always bring around a sudden spike in demand for VoIP services, since a lot of people have the idea to start up a business at the end of year. The Customer Success Circle is swamped with the workload, and Voys has decided to bring in freelancers to manage the heavy traffic.

Each customer support ticket is estimated to take a certain number of seconds to resolve, and these tickets are bundled into tasks. Each task may contain one or more tickets, and each group of tickets is assigned to a specific customer support agent or a freelancer.

Voys needs to identify which customer support agent is currently handling the heaviest workload to effectively allocate the freelancers' time. As a Voys engineer, you're tasked with analyzing the data and ensuring that the help is sent where it's needed most.

For example, if you have the following the data:

```
1200 # Estimated amount of seconds
3000
450

5000

3200
2500

2100
1300
1100

10000
```

Here, each section of numbers is separated by a blank line, representing different support agents. The program you've written has calculated and found that there is a customer support agent with 10000 seconds of ticket time, and this is the most workload which can be found.

_**Determine the highest total workload in seconds.**_
