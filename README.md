
# Ethereum Private Key Balance Checker

This Python script checks the balance of Ethereum addresses generated from a list of private keys. It connects to the Ethereum mainnet via Infura and saves addresses with a balance greater than 0.10 ETH to a file.

## Features
- Check the balance of Ethereum addresses generated from private keys.
- Multi-threaded for faster processing.
- Save results to files:
  - `good +0.1 eth.txt`: Addresses with a balance greater than 0.10 ETH.
  - `good -0.1 eth.txt`: Addresses with a balance less than or equal to 0.10 ETH.

## Prerequisites
Before using this script, ensure you have the following:
1. **Python 3.x** installed on your machine.
2. An **Infura account** with a project ID (for Ethereum node access).
3. A text file containing a list of private keys (one per line).

## Installation
1. Clone this repository (if applicable):
   ```bash
   git clone https://github.com/moxonx/eth_private_key_brute_force.git
   cd ethereum-balance-checker
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration
1. Replace the Infura URL in the script with your own Infura project URL:
   ```python
   w3 = Web3(Web3.HTTPProvider("https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID"))
   ```
2. Prepare a text file (e.g., `private_keys.txt`) containing a list of private keys, one per line:
   ```
   0xYourPrivateKey1
   0xYourPrivateKey2
   0xYourPrivateKey3
   ```

## Usage
1. Run the script:
   ```bash
   python check_balances.py
   ```
2. When prompted, enter the path to your private key file (e.g., `private_keys.txt`).
3. The script will:
   - Check the balance of each address.
   - Print the private key, address, and balance to the console.
   - Save addresses with a balance greater than 0.10 ETH to `good +0.1 eth.txt`.
   - Save addresses with a balance less than or equal to 0.10 ETH to `good -0.1 eth.txt`.

## Example Output
```
Private Key: 0xYourPrivateKey1
Address: 0xYourAddress1
Balance: 0.15 Ether
good_balance

Private Key: 0xYourPrivateKey2
Address: 0xYourAddress2
Balance: 0.05 Ether
```

## Important Notes
- **Security**: Never share your private keys or commit them to version control. Use this script in a secure environment.
- **Infura Rate Limits**: Be aware of Infura's rate limits. If you have a large number of private keys to check, consider using a dedicated Ethereum node.
- **Multi-threading**: The script uses multi-threading to speed up the process. Adjust the number of threads based on your system's capabilities.

## Disclaimer
This script is for educational purposes only. Use it at your own risk. The author is not responsible for any loss of funds or unintended consequences.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support
If you find this project helpful, consider giving it a ⭐ on GitHub. For questions or issues, please open an issue in the repository.



