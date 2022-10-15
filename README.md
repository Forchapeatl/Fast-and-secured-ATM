# Fast-and-secured-ATM

![image](https://user-images.githubusercontent.com/24577149/195977588-b8b8fc9b-447b-4cef-9111-7d8520956070.png)

One way to model the ATM logic would be as a state machine. In each state, the
thread waits for an acceptable message, which it then processes. This may result in
transitioning to a new state, and the cycle continues. The states involved in a simple
implementation are shown in figure 4.3. In this simplified implementation, the system
waits for a card to be inserted. Once the card is inserted, it then waits for the user to
enter their PIN, one digit at a time. They can delete the last digit entered. Once
enough digits have been entered, the PIN is verified. If the PIN is not OK, you’re fin-
ished, so you return the card to the customer and resume waiting for someone to
enter their card. If the PIN is OK, you wait for them to either cancel the transaction or
select an amount to withdraw. If they cancel, you’re finished, and you return their
card. If they select an amount, you wait for confirmation from the bank before issuing
the cash and returning the card or displaying an “insufficient funds” message and
returning their card. Obviously, a real ATM is considerably more complex, but this is
enough to illustrate the idea.

##State sequence diagram for our ATM machine

![image](https://user-images.githubusercontent.com/24577149/195689136-f0f57827-7a46-4326-9467-760843876ad6.png)
