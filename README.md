# free-internet-break-filters (hopefully article 13 gets canceled)
A concept on how automated git filters can be broken, since the new copyright law (Article 13) will be in place. This can be applied to any type of raw code.

## Filters? Article 13?
You can read more about article 13 here:
- https://www.saveyourinternet.eu/
- https://blog.github.com/2018-03-14-eu-proposal-upload-filters-code/

Github gave us an example of how the filter would be implemented :
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

## Concept
The concept it self would be to **obfuscate** the code being ```pushed``` using a unique key to each repository and then **de-obfuscate** on ```pull``` to make it readable again . Can be done by shifting each letters based on the key.
Each repository would generate a unique key, including old and new ones.

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
