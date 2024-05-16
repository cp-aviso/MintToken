# MintToken
Here you will see the simple way of creating token in remix
you can see the syntax inside the sol. file 

sample syntax below :

    constructor() ERC20("CarloAviso Token", "CAT") {
        owner = msg.sender;
        _mint(msg.sender, 1000000 * 10 ** decimals());
    }

    function mint(address to, uint256 amount) public {
        require(msg.sender == owner, "Only owner can mint");
        _mint(to, amount);
    }
   
