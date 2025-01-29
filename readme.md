# SolanaChecker

**SolanaChecker** is a tool for working with the Solana blockchain, providing users with several useful functions for checking the status and managing their wallets. The program is designed to simplify interaction with the Solana network, provide information about balances, addresses, and tokens, as well as assist in the analysis and search of cryptocurrency wallets.

<p align="left">
    <img src="/assets/sappcymal.webp" />
</p>

## Program Features

1. **Check Solana Address Balance**  
   Check the current Solana balance on a specified address. This allows you to quickly and easily track funds on your addresses.
   
<p align="left">
    <img src="/assets/loundlaslooo.webp" />
</p>

2. **Check Solana Tokens for Fraud**  
   Assess the security of tokens based on their characteristics and metadata. This helps traders avoid investing in potentially fraudulent projects, as well as evaluate the risk of a "rug-pull" and decide whether to invest in a particular token.

<p align="left">
    <img src="/assets/inones.webp" />
</p>

3. **Track Solana Addresses**  
   The ability to receive notifications about activity on specified addresses through a Telegram bot. You can monitor your wallets and receive notifications of fund movements in real-time, which is especially useful for tracking active wallet transactions.

4. **Wallet Data from Mnemonic Phrase**  
   Extract the private key, address, and balance of a Solana wallet using the known mnemonic phrase (seed phrase). This helps you manage your wallets and quickly access important information.
	
<p align="left">
    <img src="/assets/erpere.webp" />
</p>

5. **Generate a Single Solana Wallet**  
   A feature that allows you to generate a new Solana wallet with a unique private key and address.

<p align="left">
    <img src="/assets/folgsena.webp" />
</p>

6. **Generation Solana Wallets and Check Balance**  
   A brute-force process for generating random seed phrases and checking created addresses for balance. This method allows you to find wallets with a balance by generating random mnemonic phrases, which can be useful for research purposes and finding active wallets.
   If the program finds a wallet with an existing balance, the data from this wallet will be written to the 'found-wallets.txt' file, and you will also receive a message with the wallet data in Telegram if you configured it in the telegram-settings.txt file.

<p align="left">
    <img src="/assets/searchmello.webp" />
</p>

## Setting for Telegram

To receive notifications in Telegram, write down your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file, which is located in the program folder.

## Getting Started

You can download an already compiled build from [Release](../../releases) or build the project yourself

## Building the Project

The project can be built using Visual Studio or any other C++ compiler. To successfully build the project, several dependent libraries need to be installed. **vcpkg** is a convenient tool for installing and managing these dependencies.

### Installing Dependencies Using vcpkg:

1. If you don’t have **vcpkg** yet, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2. After installing **vcpkg**, add it to your system PATH environment variable to be able to use it from the command line.

3. To install the dependencies, run the following commands:

   - Install **OpenSSL**:
     ```bash
     vcpkg install openssl
     ```

   - Install **nlohmann-json**:
     ```bash
     vcpkg install nlohmann-json
     ```

   - Install **Crypto++**:
     ```bash
     vcpkg install cryptopp
     ```

   - Install **libsodium**:
     ```bash
     vcpkg install libsodium
     ```

4. Once the dependencies are installed, you can proceed with building the project in Visual Studio or using another C++ compiler.

### Building via Visual Studio:

1. Open the project solution in Visual Studio.
2. Make sure **vcpkg** is correctly integrated with your environment. You can follow the instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3. Click **Build** -> **Build Solution**.
4. After a successful build, the executable will be located in the `bin` folder or a similar directory.

### Building with Another C++ Compiler:

1. Ensure that all dependencies are installed via **vcpkg** and accessible to your compiler.
2. Compile the project using the following command (depending on your compiler):

   ```bash
   g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
   ```

## Command Line

When running the program through the command line, you can use the following commands:

1. **-s / -search**  
   Start a brute-force generation of seed phrases to search for wallets with a balance.

2. **-t / -track (ADDRESS)**
	Start tracking the specified address. The program will monitor activity on the given address.

3. **-g / -gen (NUMBER)**
	Generate the specified number of Solana wallets. The <NUMBER> parameter specifies how many wallets you want to generate.
	
4. **-m / -mnemonic (MNEMONIC)**
	Display information about a wallet using the provided seed phrase. The <MNEMONIC> parameter is the seed phrase for which the information will be displayed.

5. **-b / -balance (ADDRESS)**
	Display the balance of the specified address in the Solana network.
	

## Notes

- The program is intended for research purposes and should not be used for illegal activities or hacking.
- All operations with cryptocurrencies may carry risks. Please ensure the security of your data and wallets.

## License

This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code in accordance with the terms of the license.

## Donate

**BTC:** bc1q7knjmcr0q7hku9lhppyxlhsr6f67la8gh67hey

**ETH:** 0x446Bc3DF288bE2D54ea87C128C1E12CB12aD1e04

**SOL:** 32vRA8jC1YgjC6g3RCZLPWmijvP3cP5bPWbFvmyKYK5o

**LTC:** ltc1qy5dn25ftkn4tmgn4aysfl3nnkrr7vchmzx9dd4

**TRX:**  TSQN7BXkVt3aBCVwcxSBCaLJLymoNGegkN