# go-andotp
CLI program to encrypt/decrypt [andOTP](https://github.com/andOTP/andOTP) files.

## Installation
```
$ go get github.com/grijul/go-andotp
```

## Usage
```
Usage: go-andotp -i <INPUT_FILE> {-e|-d} [-o <OUT_FILE>] [-p PASSWORD]

  -d    Decrypt file
  -e    Encrypt file.
  -i string
        Input File
  -o string
        Output File. If no file is provided, output is printed to STDOUT
  -p string
        Encryption Password. This option can be skipped to get password prompt.
```

## Examples
- Encrypt JSON file (Password is asked after hitting ```Enter```. Password is not echoed)
```
$ go-andotp -e -i file.json -o file.json.aes
```
- Encrypt JSON file (Password is entered through CLI)
```
$ go-andotp -e -i file.json -o file.json.aes -p testpass
```
- Decrypt JSON file
```
$ go-andotp -d -i file.aes.json -o file.json
```
- Decrypt JSON file and print json to console
```
$ go-andotp -d -i file.aes.json
```

# License
[MIT](https://github.com/grijul/go-andotp/blob/main/LICENSE)
