# cps472-572-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [CPS472_572 Assignment 1 Solved](https://www.ankitcodinghub.com/product/cps472_572-assignment-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90921&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CPS472_572 Assignment 1 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
1. Purpose

This homework builds an understanding of classic block ciphers and cryptanalytic attacks.

2. Description 2.1. TEA

The Tiny Encryption Algorithm (TEA) block cipher operates on 64-bit blocks of plaintext using a 128-bit key. The plaintext is divided into two 32-bit blocks (L0, R0), and the key is divided into four 32-bit blocks (K0, K1, K2, K3). Encryption involves repeated application of two Feistel rounds (making up one cycle of TEA), defined as follows for round i and i+1:

</div>
</div>
<div class="layoutArea">
<div class="column">
Li = Ri-1 Ri = Li-1 Li+1 = Ri Ri+1 = Li

</div>
<div class="column">
F(Ri-1, K0, K1, δi); F(Ri, K2, K3, δi+1);

</div>
<div class="column">
Li-1 Ri-1

Li Ri

</div>
</div>
<div class="layoutArea">
<div class="column">
where

shift of x by y bits is denoted by x &lt;&lt; y, the logical right shift of x by y bits is denoted by x &gt;&gt; y, δi is a sequence of predetermined constants, and F is defined as

</div>
</div>
<div class="layoutArea">
<div class="column">
denotes modulus +, the logical left

</div>
</div>
<div class="layoutArea">
<div class="column">
F(X,Kj,Kk,δi )=((X&lt;&lt;4) Kj) ⊕ ((X&gt;&gt;5) Kk) ⊕ (X+δi).

The encryption function is given next, written in C, for encoding with key k[0] … k[3]. Data is in v[0] and v[1] and there are 32 cycles (i.e., 64 rounds).

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
void code(unsigned long* v, unsigned long* k) {

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
2.2. Attack Method

In this project, we will develop a C++ program that performs an attack on 1 round of TEA. In 1 round of TEA the key size is effectively reduced to 64 bits, because only half of the 128 bit key is used in 1 round of TEA. Using known plaintexts and their resulting ciphertexts, we will perform a brute force attack on the 64-bit key by repeatedly guessing 32 bits of the key, which will eventually lead us to deduce the other 32 bits.

We only need to search through 232 possible keys, since given a subkey K0, we can calculate a value for the other subkey K1 by using known plaintext/ciphertex pairs (i.e., derive an equation for K1 in terms of K0 and a pair of plaintext/ciphertext).

In this project, first implement the TEA encryption method and then generate 100 random plaintexts and their corresponding ciphertexts using 1 round of TEA encryption (see Figure below). That is, each plaintext is &lt;L0, R0&gt; and its corresponding ciphertext is simply &lt;L1, R1&gt;. Output the plaintext/ciphertext pairs to a file.

L0 R0

L1 R1

The following steps/pseudocode outline the general procedure of the attack program.

1. Read in the file with the plaintext/ciphertext pairs into lists. These values are then converted from strings in the file to 32 bit unsigned integers.

2. Guess a value for subkey K0, starting at 0.

3. Calculate the value for K1 using our guess K0 and the first plaintext/ciphertext pair.

4. Calculate the value for K1 using our guess K0 and the second plaintext/ciphertext pair. 5. Do those two values of K1 match?

6. If not, this is the incorrect guess for K0. Increment our guess and go back to Step 3. 6. If yes, we need to verify that this guess for subkey K0 is correct

7. Repeat steps 3 and 4 ten times with different plaintext/ciphertext pairs

8. If the values of K1 did not match every time, increment our guess for K0 and go back to Step 3.

9. If the values of K1 matched every time, this is the correct guess for K0 and we’ve found the key!! Print the key and the run time of your project.

</div>
</div>
</div>
