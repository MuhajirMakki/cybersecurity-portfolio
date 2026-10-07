# Score Risks Based on Likelihood and Severity

## Project Description

In this activity, I practiced performing a cybersecurity risk assessment for a commercial bank. I reviewed different risks affecting the bank's funds and scored each risk based on its likelihood and severity.

The overall priority was calculated using:

**Likelihood × Severity = Priority**

## Scenario

The bank operates in a coastal area with low crime rates. It has 100 on-premise employees and 20 remote employees, along with 2,000 individual customer accounts and 200 commercial accounts.

The bank also works with a professional sports team and ten local businesses. Because financial data and funds are handled by many people and systems, there are different risks that could affect the bank's operations and information.

## Risk Assessment

| Asset | Risk                      | Description                                                         | Likelihood | Severity | Priority |
| ----- | ------------------------- | ------------------------------------------------------------------- | ---------: | -------: | -------: |
| Funds | Business email compromise | An employee is tricked into sharing confidential information.       |          2 |        2 |        4 |
| Funds | Compromised user database | Customer data is poorly encrypted.                                  |          2 |        3 |        6 |
| Funds | Financial records leak    | A database server containing backed-up data is publicly accessible. |          3 |        3 |        9 |
| Funds | Theft                     | The bank's safe is left unlocked.                                   |          1 |        3 |        3 |
| Funds | Supply chain disruption   | Delivery delays caused by natural disasters.                        |          1 |        2 |        2 |

## Risk Factors

Doing business with other companies can increase the risk to the bank's data because it creates additional ways for information to be compromised. The risk of theft is also important, but the bank's low-crime location makes it less likely compared with some of the other risks.

## Likelihood

I scored each risk from 1 to 3 based on how likely the event is to occur.

* **1 — Low likelihood**
* **2 — Moderate likelihood**
* **3 — High likelihood**

The financial records leak received a likelihood score of **3** because a publicly accessible database can be easily exposed. Business email compromise and a compromised user database received **2** because these incidents are reasonably possible in an environment with many employees and systems.

Theft and supply chain disruption received **1** because the bank is located in an area with low crime rates and natural disasters are less predictable.

## Severity

I also scored each risk from 1 to 3 based on the potential impact on the bank.

* **1 — Low severity**
* **2 — Moderate severity**
* **3 — High severity**

The compromised user database, financial records leak, and theft received a severity score of **3** because these events could cause major financial, operational, regulatory, or reputational damage.

## Priority

The priority score was calculated by multiplying likelihood by severity.

The **financial records leak** received the highest priority score of **9**. This means it should receive significant attention because it has both a high likelihood and a high potential impact.

The compromised user database received a score of **6**, followed by business email compromise with **4**, theft with **3**, and supply chain disruption with **2**.

## What I Learned

This activity helped me understand how cybersecurity teams use risk assessments to prioritize security issues. A risk with a higher likelihood and greater impact should generally receive attention before lower-scoring risks.

I also learned that risk scoring is not only about how dangerous a threat is. The likelihood of the event and the potential impact on the organization both need to be considered.

## Cybersecurity Connection

Risk registers help security teams keep track of vulnerabilities and potential security incidents. They can also help organizations decide where to focus their security resources first.

For a security analyst, understanding likelihood, severity, and priority is useful when identifying and communicating the most important risks to an organization.

## Conclusion

I completed a risk assessment for the bank by evaluating five risks and assigning likelihood, severity, and priority scores. The highest-priority risk was the financial records leak, with a score of **9**.

This activity gave me practice with a basic risk assessment process and showed how organizations can use risk scores to prioritize cybersecurity efforts.
