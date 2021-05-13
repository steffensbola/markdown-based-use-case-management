# Use Case Name: Transfer Funds

*Important: This use case example is adapted from an example created by Tony Loton, available [here](https://www.modernanalyst.com/Resources/Articles/tabid/115/ID/2016/End-to-End-UML-Use-Case-Specification.aspx).*

1. Brief Description  
The Transfer Funds use case allows a banking Customer to transfer money from one of his (or her) bank accounts to another ; or the Bank Manager to transfer funds between any two accounts on behalf of a Customer.

1. Actor(s)  
Customer, Bank Manager

# Flow of Events

## Basic Flow
The flow of events – which involves the actor selecting two accounts, entering an amount to transfer, and the funds transfer taking place – has been formalized in the following event sequence so as to facilitate the realization of this use case as one or more UML Sequence Diagrams.

1. The Customer (or Bank Manager) actor selects the Source Account via the Select Account use case which this use case `<<uses>>` or `<<imports>>`.  

2. The Customer (or Bank Manager) actor selects the Destination Account via the Select Account use cases.  

3. The actor enters an amount to transfer and confirms by pressing the Proceed button.  

4. The Source Account incurs a debit of the required amount.  

5. The Destination Account receives a credit of the specified amount.  

## Alternative Flows  

1. First Alternative Flow
The actor may cancel the funds transfer by pressing the Cancel button rather than the Proceed button at step 3; in which case the use case ends.  

# Special Requirements  

1. First Special Requirement  
In order to comply with money laundering regulations, all inter-account transfers are limit to a maximum of $10,000. This system-wide amount may be varied as specified in business rule #1.  

# Pre-Conditions  

1. First Pre-Condition  
The actor must be logged into the banking web application via the Internet (for the Customer actor) or the bank intranet (for the Bank Manager actor).

# Post-Conditions  

1. First Pre-Condition  
The total of the funds in the Source Account plus Destination Account must be the same when the use case concludes as it was before the use case began. No money should have been ‘lost in transit’, for example by having been debited from the Source Account yet not successfully credited to the Destination Account.

# Extension Points  

1. First Extension Point: Insufficient Funds  
This extension is invoked if there are insufficient funds in the Source Account for the transfer to the Destination Account.  

2. Second Extension Point  
This extension is invoked to freeze the accounts and to log an error if the integrity of the total funds across both accounts has not been preserved during the transaction.  