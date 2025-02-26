# Guess-Bitcoin-Private-Key

This is version is forked from scorta/GuessPrivateKey, many thanks for his project.

The error * SLF4J: Failed to load class "org.slf4j.impl.StaticLoggerBinder".
            SLF4J: Defaulting to no-operation (NOP) logger implementation
            SLF4J: See http://www.slf4j.org/codes.html#StaticLoggerBinder for further details.* 
has been gone.

USAGE
Install java on your computer, download the GuessPrivateKey.jar file, then enter this command:

$java -jar {this_program} {numbers of threads} {file_contains_bitcoin_addresses} {choice} {start_from}

Parameters:
{numbers of threads}: number of threads, should be equal to your CPU cores (or less, if you want to use it for other tasks). Eg. my CPU has 8 cores, so I set {numbers of threads} to 8.
{choice}: random means guessing keys randomly; up means checking for {start_from} and upper. down means going down from {start_from}.
{start_from}: Starting number. Default value is 0.
Sample commands:

$java -jar GuessPrivateKey.jar 7 bit.txt
# 7 threads, searching randomly for list of address(es) in the file bit.txt

$java -jar GuessPrivateKey.jar 8 bit.txt up 666
# searching sequentially from 666 and upper

$java -jar -Xmx6g GuessPrivateKey.jar 8 bit.txt up 666
# set maximum memory allocation pool to 6GB

If you have a big list of Bitcoin addresses (like, millions), you may need to use the -Xmx option. Eg. for a 1GB input file, I'd like to use 6GB memory (RAM), as the command above.

OUTPUT
If found a key, the program will display a message "Found a key!!!", and print info to a file, which has the same name to that WIF key.
Eg. if it found the key "L59eMgqKqxCGXrDWhGwVBZbQBra482LRLzyAj6g5CGKdq6ABCvXz", it will create a file name "L59eMgqKqxCGXrDWhGwVBZbQBra482LRLzyAj6g5CGKdq6ABCvXz.txt" and write these info into it:

1zJBmcSDHZ97Sjm6TmtM5M7ZdPzuiBABm //address
L59eMgqKqxCGXrDWhGwVBZbQBra482LRLzyAj6g5CGKdq6ABCvXz //key in WIF format
EC9B83954E3E5001E34B02A1705779D2B59264BB54784815B3AA3EBC10C622F0 //key in HEX format

So if you find a new .txt file in the same folder with this program, you have found a wallet!
Note: if it cannot create file(s), it will print these info directly into the screen. 
Below the screen shoot of Working Proof

![GuessPrivateKey_LI](https://github.com/user-attachments/assets/cb3615ce-0230-438d-b708-0eff192cfd66)

if you like my project please tips me here :

USDT (BEP20) 0xe5ebfa618d84ac0e17b65ed49103bf9ad9458b17

BTC 18TxFasTh5rBNe5pRrHULvKEbtxArRfkU3

DOGE DQp2mRMwe6QY6BxoodHsqziYJacrHNkJ9Q

ETH 0xe5ebfa618d84ac0e17b65ed49103bf9ad9458b17

copyright©2024-2025 Manuklondong™
