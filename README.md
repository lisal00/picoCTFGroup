# picoCTF

## Fantasy CTF: 
picoCTF{m1113n1um_3d1710n_76b680a5}  </br>
Nc in using the given command <code>nc verbal-sleep.picoctf.net 63159</code>. Pressed enter when prompted and answered the questions correctly. Flag was given at the end when all questions were answered

## Cookie monster secret recipe: 
picoCTF{c00k1e_m0nster_l0ves_c00kies_98D0603F} </br>
Went to the website, and tried to log in using random log ins and passwords. The next page said to check the cookies, so I used inspect element and went to storage to find the cookies. There was a value called secret_recipe cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzXzk4RDA2MDNGfQ%3D%3D. It was encoded in base64. Decoding gave the flag.

## head-dump:
picoCTF{Pat!3nt_15_Th3_K3y_ad7ea5ae} </br>
Went to the website, and only one hastag led to another part of the website, which was the api documentation. It led to Swagger, which had an endpoint called head dump. Executing it generated a file, and searching through it had the flag. 
