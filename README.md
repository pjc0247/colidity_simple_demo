# colidity_simple_demo

https://pjc0247.github.io/colidity_simple_demo/

```cs
public class ERC20
{
    public event Action<address, address, uint256> Transfer;
    private mapping<address, uint256> balances = new mapping<address, uint256>();
    
    public void transfer(address sender, address recipient, uint256 amount)
    {
        contract.require(sender != null);
        contract.require(recipient != null);

        balances[sender] = SafeMath.Sub(balances[sender], amount);
        balances[recipient] = SafeMath.Add(balances[recipient], amount);

        Transfer(sender, recipient, amount);
    }
}
```
