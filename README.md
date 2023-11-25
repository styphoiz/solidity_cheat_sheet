```
contract Example{
    function example1() private pure {
        // private: call me within this contract
        // pure: I cannot read/write to storage
    }
    function example2() internal view {
        // internal: call me within this contract (+ inheritance!)
        // view: I can read from storage, not write 
    }
    function example3() public payable {
        // public: call me inside and outside this contract
        // payable: send me some ether!
    }
    function example4() external {
        // external: call me from outside this contract
    }
    function example5() public virtual {
        // virtual: override a function within a contract
    }

    receive() external payable{
        // no calldata necessary here
        // just send a value on the message call
    }
    function pay() external payable {
        // in this case, we target pay with a value
    }
}
```
