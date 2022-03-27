# Cryptanalysis-Project
### Break an encryption by finding the key through a weakness in the random number generation
 
This program finds the seed used to generate the encryption key (when generated with a weak Pseudo Random Number Generator) used to encrypt plaintext with the DES encryption algorithm. 

We assume that the user already has access to a ciphertext and plaintext and the daterange when key was created. The program iterates over the given daterange (minute resolution) and uses each datetime object as the seed to generate the encryption key. The generated ciphertext (on each iteration) is then compared to the ciphertext provided by the user. If a match occurs, the program will output the seed used for the key generation. 

### Instructions
* Create a .NET project with the attached .cs file
* Run the following command ```dotnet run "Hello World" "RgdIKNgHn2Wg7jXwAykTlA==" "7/3/2020/11/00-7/4/2020/11/00""```
  * arg0 = plaintext
  * arg1 = ciphertext
  * arg3 = daterange
* Program will output any matching seed, for example: ```26564295```

Console Example:
```
$ dotnet run "Hello World" "RgdIKNgHn2Wg7jXwAykTlA==" "7/3/2020/11/00-7/4/2020/11/00"

plain_text: Hello World
cipher_text: RgdIKNgHn2Wg7jXwAykTlA==
date_range: 7/3/2020 11:00:00 AM - 7/4/2020 11:00:00 AM

seed: 26564295
```
