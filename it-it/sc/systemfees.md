# Sistema di Tassazione

## Tassa di transazione

Al momento non vi sono commissioni sulle transazioni. L'utente puó comunque scegliere di pagare la tassa della transazione per avere prioritá.

## Tassa per smart contract

La struttura di tassazione per gli Smart Contracts puó essere trovata nella tabella sotto.

Gli iniziali 10 GAS sono sempre gratuiti. Le tasse che ammontano a 10 GAS o meno non richiedono alcun servizio di commissione.

Le tasse seguenti sono commissioni minime. L'utente puó decidere di pagare qualcosa in piú per avere prioritá.

Tutte le tasse degli smart contract sono considerate come servizio di tassazione da mettere in una pool per la redistribuzione a tutti i possessori di NEO. La distribuzione é proporzionale alla quantitá di NEO.

### Tassazioni per le Chiamate al Sistema

| SysCall                               | Tassa [Gas]     |
|---------------------------------------|:-------------:|
| Runtime.CheckWitness                  | 0.2           |
| Blockchain.GetHeader                  | 0.1           |
| Blockchain.GetBlock                   | 0.2           |
| Blockchain.GetTransaction             | 0.1           |
| Blockchain.GetAccount                 | 0.1           |
| Blockchain.GetValidators              | 0.2           |
| Blockchain.GetAsset                   | 0.1           |
| Blockchain.GetContract                | 0.1           |
| Transaction.GetReferences             | 0.2           |
| Account.SetVotes                      | 1             |
| Validator.Register                    | 1000          |
| Asset.Create (system asset)           | 5000          |
| Asset.Renew (system asset) [per anno] | 5000          |
| Contract.Create                       | 500           |
| Contract.Migrate                      | 500           |
| Storage.Get                           | 0.1           |
| Storage.Put [per KB]*                 | 1             |
| Storage.Delete                        | 0.1           |
| (Default)                             | 0.001         |

* Aggiuntivo 1 GAS minimo.

### Tassazioni per le Istruzioni

| Istruzione                           | Tassa [Gas]     |
|---------------------------------------|:-------------:|
| OpCode.PUSH16 [or less]               | 0             |
| OpCode.NOP                            | 0             |
| OpCode.APPCALL                        | 0.01          |
| OpCode.TAILCALL                       | 0.01          |
| OpCode.SHA1                           | 0.01          |
| OpCode.SHA256                         | 0.01          |
| OpCode.HASH160                        | 0.02          |
| OpCode.HASH256                        | 0.02          |
| OpCode.CHECKSIG                       | 0.1           |
| OpCode.CHECKMULTISIG [per firma]  | 0.1           |
| (Default)                             | 0.001         |

