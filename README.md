## VerboseVerify
A neo-cli plugin to provide extended information about transaction verification failures during the `sendrawtransaction` RPC method

### Introduction
There are 20+ reasons a Neo transaction may fail verification, but the Neo RPC server by default only gives generic
error messages, such as the dreaded "Transaction or block verification failed", leaving the developer to figure out
exactly what is wrong with their transaction syntax. VerboseVerify plugin intercepts `sendrawtransaction` requests
and runs them through the same transaction verification process used by the Neo core, except it provides specific
information about what specific failure condition was encountered.

### Installation
```
git clone https://github.com/Splyse/VerboseVerify
cd VerboseVerify
dotnet publish -c Release
cp ./bin/Release/netstandard2.0/publish/VerboseVerify.dll {neo-cli folder}/Plugins
```

### Configuration
No configuration required.
