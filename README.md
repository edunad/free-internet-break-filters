# free-internet-break-filters (v0.0.1)
A concept on how **automated git filters** can be **broken**, since the new copyright law (Article 13) will be in place. This can be applied to any type of raw code.

## Automatic Filters? Article 13?
I recommend reading more about article 13, here are some resources:
- https://www.saveyourinternet.eu/
- https://blog.github.com/2018-03-14-eu-proposal-upload-filters-code/
- https://youtu.be/Sm_p3sf9kq4 (more serious video)
- https://youtu.be/89ZkydX0FPw (less serious video)

Github gave us an **example** on how the filter would be implemented :
```
$ git push 
...
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: error: GH013: Your push could infringe someone's copyright.
remote: If you believe this is a false positive (e.g., it's yours, open
remote: source, not copyrightable, subject to exceptions) contact us:
remote: https://github.com/contact
remote: We're sorry for interrupting your work, but automated copyright
remote: filters are mandated by the EU's Article 13.
To github.com/vollmera/atom.git
 ! [remote rejected] patch-1 -> patch-1 (push declined due to article 13 filters)
 ```

## The Concept
The concept it self would be to **obfuscate** the code being ```pushed``` using a unique key to each repository and then **de-obfuscate** on ```pull``` to make it readable again. This can be done by shifting each letter based on the **repository key**.

Each repository would generate a unique key.

### QA
> "Would this break the hosting website? For example github?"
- Github could then read the **repository key** and use it to display the corrected text (check the 4th line, for alternatives)

> "What about the local code? Or automated builds?"
- The local code would never be affected, since it's **de-obfuscated** when pulled. Automated build services would use the **repository key**

> "What if, i clone the repository? Would i be able to contribute?"
- When you **clone/checkout/fork** the repository, you would also **clone the repository's key**, allowing you to **de-obfuscate** the code and make your changes.

> "What if, the hosting websites are forced by law to **de-obfuscate** the code and then filter it?"
- If that happens, then the repository key would need to be hosted somewere else. This would then break the hosting website, and you would be required to use a **program** to manage pull requests using your machine.

# Concept example
Code before being pushed :
```
function helloWorld() { console.log('helloworld'); }
```

Code after being pushed (this is how the uploaded file would look like)
```
Repository key: 3g348hfkjd

gftjrejr fghtkeivmr() { fsghyyg.sdf('sdgjtkmvkt'); }
Note: On this example it's just random letters. Using the repository key 'a' would be 'k', 'b' would be 'f', etc.
```

## Feel free to contribute/improve/share this concept!
