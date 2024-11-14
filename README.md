Decentralized Ticket Reselling Platform
Overview
The Decentralized Ticket Reselling Platform is a Solidity-based smart contract that enables secure and transparent peer-to-peer ticket reselling for events. It provides a decentralized solution for event organizers, ticket holders, and buyers to facilitate the resale of tickets while ensuring ticket authenticity and preventing fraud.
Key Features

Event Creation: Event organizers can create new events, specifying the event details such as event name, total tickets, ticket price, and event time.
Ticket Purchase: Buyers can purchase tickets directly from the event organizers at the specified ticket price.
Ticket Resale: Ticket holders can list their tickets for resale, setting a resale price within the maximum allowed limit.
Secure Transactions: The contract implements fraud prevention mechanisms to ensure ticket authenticity and secure peer-to-peer transactions.
Commission-based Model: The contract charges a 10% commission on each ticket resale, which is distributed between the event organizer and the contract's developer.

Contract Structure
The contract consists of the following key components:

Ticket struct: Represents a ticket, including the owner, sale status, and resale price.
Event struct: Stores the event details, such as event name, ticket price, maximum resale price, total tickets, and event time.
createEvent(): Allows event organizers to create a new event.
buyTicket(): Enables buyers to purchase tickets directly from the event organizer.
listTicketForResale(): Allows ticket holders to list their tickets for resale.
buyResaleTicket(): Facilitates the purchase of a resale ticket by a new buyer.
getTicketOwner(): Provides a function to retrieve the current owner of a ticket.

Security and Fraud Prevention
The contract implements the following measures to ensure security and prevent fraud:

Ownership Verification: The onlyOwner modifier ensures that only the ticket owner can list the ticket for resale.
Resale Price Limit: The maxResellPrice variable limits the maximum resale price to 130% of the original ticket price.
Event Start Time Check: The eventNotStarted modifier prevents ticket resale within 30 minutes of the event start time.

Usage
To use the Decentralized Ticket Reselling Platform, follow these steps:

Deploy the contract to the Ethereum network.
Event organizers can call the createEvent() function to set up a new event.
Buyers can call the buyTicket() function to purchase tickets directly from the event organizer.
Ticket holders can call the listTicketForResale() function to list their tickets for resale.
Buyers interested in resale tickets can call the buyResaleTicket() function to purchase the tickets.

License
This project is licensed under the MIT License. CopyRetryClaude does not have internet access. Links provided may not be accurate or up to date.
