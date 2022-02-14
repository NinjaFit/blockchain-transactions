# SGC - Blockchain Transactions Challenge

Someone tipped us a csv file containing thousands of transactions from a new blockchain developed and used by the Moonshot Satellites employees, KolluCoin.

This `transactions.csv` file contains the following variables:

- `date/time`: The date and time the transaction happened.
- `transaction_id`: An eight number id representing the recorded transaction.
- `transaction_hash`: A SHA-256 encrypted hash representing the recorded transaction.
- `to_address`: The address that performed the transaction (encoded in base58).
- `from_address`: The address on the receiving end of the transaction (encoded in base58).

We believe this file may contain some useful information and potentially include addresses coming from the hacker group Unwanted Guest. Our guess is that the most suspicious addresses are the ones that are conducting the most transactions.

Your **goal** on this challenge is to analyze this dataset and find the two addresses that conduct the most transactions between each other.

1. If address `A4HgDFaa` sends KolluCoin to address `BhGu48Nb`, that is considered as 1 transaction, the same goes for the other way around where address `BhGu48Nb` sends KolluCoin to address `A4HgDFaa`, also considered 1 transaction.

2. If you find the two suspicous addresses, decode them from `base58` to `utf-8` to get the encrypted word of the address. For example, `'99p6wEQ'` => `'HAPPY'`

Here is the format of the flag: `FLAG{700:ADDRESS1ADDRESS2}`

- `ADDRESS1` is one of the addresses you decrypt.
- `ADDRESS2` is the other address you decrypt.

Example flag: `FLAG{700:SPACEHAPPY}`

Save this flag so that you can submit it during the competition! Happy exploring!

## Dependencies

Here are two dependencies that may make your life easier (Python):

- [Pandas](https://pandas.pydata.org/)
- [Base58](https://pypi.org/project/base58/)

## Environment

You don't have to, but Jupyter Notebooks are a great way to handle data science environments. Feel free to set up an environment either [locally](https://jupyter.org/install) or through [Google Collab](https://colab.research.google.com/) to perform your analysis.
