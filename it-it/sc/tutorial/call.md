# Chiamata al Contratto

```c#
[AppCall("XXXXXXXXXX")] // ScriptHash
public static extern int AnotherContract (string arg);

public static void Main ()
{
     AnotherContract ("Hello");
}
```

In uno smart contract, puoi usarla per chiamare altri smart contracts che sono stati pubblicati sulla chain.
1. Aggiungi la dichiarazione usando AppCall e l'hash dello script del contratto per essere invocato.
2. Chiamalo nel codice.
