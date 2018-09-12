# free-internet-break-filters
A concept on how automated git filters can be broken, since the new copyright law will be in place. This can be applied to any type of raw code

## Concept
The concept it self would be to **obfuscate** the code being ```pushed``` using a unique key to each repository and then **de-obfuscate** to make it readable again it on ```pull```. Can be done by shifting each letters based on the key.



> "But this will break the website, for example github"
- Github could then read the **repository key** and use it to display the corrected text.

> "What about our local code? Or automated builds?"
- The local code would never be affected, since it's **de-obfuscated** when pulled. Automated build services would use the **repository key**

# Example 
Code before being pushed :
```
function helloWorld() { console.log('helloworld'); }
```

Code after being pushed (this is what the files would contain, inside git)
```
Repository key: 3g348hfkjd

gftjrejr fghtkeivmr() { fsghyyg.sdf('sdgjtkmvkt'); }
Note: On this example it's just random letters, but the on the actual code 'a' would be 'k' based on the repository key.
```

## Feel free to contribute with ideas, or improve this document.
