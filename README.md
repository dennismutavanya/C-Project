Banking Application
Overview
This is a simple banking application that includes two types of accounts: Group Account and Personal Account. Each account can have multiple members, and transactions such as deposit and withdrawal can be performed.

Classes
1. Member
Represents an individual member associated with an account.

Attributes:
phone: Phone number of the member.
pin: Personal Identification Number (PIN) for transactions.
isApproved: Approval status for withdrawal transactions.
Methods:
Member(string _phone, string _pin): Constructor to initialize a member with a phone number and PIN.
2. Account
An abstract class representing a generic bank account.

Attributes:
accountName: Name of the account.
members: List of members associated with the account.
Methods:
Account(string _accountName): Constructor to initialize an account with an account name.
addMember(string phone, string pin): Adds a new member to the account.
3. GroupAccount
Inherits from the Account class and represents a group account.

Methods:
GroupAccount(string _accountName): Constructor to initialize a group account with an account name.
deposit(): Performs the deposit operation.
withdraw(): Initiates a withdrawal request and seeks approval from all members.
4. PersonalAccount
Inherits from the Account class and represents a personal account.

Methods:
PersonalAccount(string _accountName): Constructor to initialize a personal account with an account name.
deposit(): Performs the deposit operation.
withdraw(): Performs the withdrawal operation.
Usage
Create instances of GroupAccount and PersonalAccount.
Add members to the group account using the addMember method.
Perform deposit and withdrawal operations on both group and personal accounts.
For group accounts, withdrawal requests will be sent to all members for approval.
