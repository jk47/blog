# Removing Passwords from Git History

When someone checks in a password in git, security is compromised. When you realize you need to fix this, the obvious first step is to rotate the passwords that have been exposed. Then you'll want to change the code to not contain the passwords. The passwords will still exist in your history though, and while they have been rotated and the security risk is alleviated, in order to stay off of someone's 'list' who may be watching your repo, you will want to remove the passwords from your history as well. 

This [tool](https://rtyley.github.io/bfg-repo-cleaner/) is [recommended](https://help.github.com/articles/removing-sensitive-data-from-a-repository/) by github. It is fairly straight-forward to use. You download a jar and execute with some parameters according to what you want to remove. In the case of removing passwords you'll end up wth a before and after similar to the one shown below. 

```
//before
ImportantPassword=p@$$word123

//after
ImportantPassword=***REMOVED**
```

