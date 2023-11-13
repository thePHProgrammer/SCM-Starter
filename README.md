# SmartContractManagement

## Contract Details

### Functions

#### `constructor(uint initBalance)`

- Description: Initializes the contract with an initial balance provided during deployment.
- Parameters:
  - `initBalance` (uint): The initial balance of the contract.
- Modifiers:
  - None

#### `getBalance()`

- Description: Retrieves the current balance of the contract.
- Returns:
  - `balance` (uint256): The current balance of the contract.
- Modifiers:
  - None

#### `deposit(uint256 _amount)`

- Description: Allows the owner to deposit funds into the contract.
- Parameters:
  - `_amount` (uint256): The amount to deposit.
- Revert Conditions:
  - Requires the caller to be the owner of the contract.
- Emits:
  - `Deposit(uint256 amount)`: Event indicating the deposit amount.
- Modifiers:
  - None

#### `withdraw(uint256 _withdrawAmount)`

- Description: Allows the owner to withdraw funds from the contract.
- Parameters:
  - `_withdrawAmount` (uint256): The amount to withdraw.
- Revert Conditions:
  - Requires the caller to be the owner of the contract.
  - Reverts if the contract has insufficient balance for the withdrawal amount.
- Emits:
  - `Withdraw(uint256 amount)`: Event indicating the withdrawal amount.
- Modifiers:
  - None

#### `burn(uint256 _burnAmount)`

- Description: Allows the owner to burn (destroy) a specified amount of tokens.
- Parameters:
  - `_burnAmount` (uint256): The amount to burn.
- Revert Conditions:
  - Requires the caller to be the owner of the contract.
  - Reverts if the contract has insufficient balance for the burning amount.
- Emits:
  - `Burn(address indexed burner, uint256 amount)`: Event indicating the burning action.
- Modifiers:
  - None
