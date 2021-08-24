# sourcetree-github-setup
Starting from 2021/8/13 you will get some error messages like this when you push the code...
```
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
```
Follow the steps below to fix it.

## Generate access token
1. Go to https://github.com/settings/tokens
2. Click `Generate new tocken`
3. Check `admin:public_key` both read and write.
4. Note, enter "sourcetree" (or whatever you like)
5. Click `Generate tocken`. Keep the access tocken.

## Add account to sourcetree
1. I am using sourcetree mac app.
2. Find your Github account
Auth Type: `Basic`
Username: Enter your user name. For me its `wuduhren`.
Password: Enter the access tocken you get in the last step.
Protocal: `SSH`
3. Click `Copy to Clipboard`. Keep this public key. Something like below:
  ```
  ssh-rsa AAAAB3NzaC1yc2EAAAADAQAfgks6AQDBfiR2y+gH7bcMdZodXpK2fI0BCGm+TvWB1QNwGlu+3JX1chFE7C+LVIkg6KlJVNHg+Q/BE3ljI1KoPvPu0bFs4DXHYZMtJTZ7cmwjtWBldsnTUd0/Sgo/agmvvvyU7jKWCy2+PJlRdyeHM7/X5FFFiVDCzhyGWG+foOdhnuIaIbgeP9I+ShYbJwpceF35owqEhw9v2XuXjx7uK5OEplNBmpVEe0f2ZU6kQoI8DXpCNUvP7C69Pk/741V7l9dMjQToZmdj8vsAcSG+zfzustyzqaMpRjWmX2oTsdfgDw0P41GRDJLm4B5b2DggdTLL3GGGTu3b9SVO58Y+rujARS+6FcmbRUQUj48QmC6IUsrfe6XW6Qq4LZ64oo3wawOEkGg/HWPxpoP86C0JaR0CCagQkiuz8a7Dho0lYllGOiXQdP8gHAiW16KdT5kYWl/v/5dtbGwVoqHkjlFq2nn0W+3gNhQ1VyMGT6rL9mTow2juVmhCs/OzxhK/SP1FFFQGS62cWIic328wVyj3lUY6e8UTbXBcpu3W5gTkPrm0DLR3TQs60QPCavr5qiXCroswC+4bh+J9Z0Jz0sXEeX0G5IwHrQDO92P29S3Pvj6XalfR9am8/3G/E6Jaz/bOgO3QSvBljq86o8wiu4YyPTL7XDbdyj/wOrT2RpM6U3/9nXww==
  ```

4. Save.

## Add public key to Github
1. https://github.com/settings/keys
2. Click `New SSH Key`.
3. Title enter: "sourcetree" (or whatever you like).
4. Paste the public key you get in the last step.
5. Click `Add SSH Key`

## Change Repo Remote Url to SSH
If you are using sourcetree mac app, go to your repo. Click `Repository` above -> `Repository Settings` -> `Remotes`
Chagne the url to something like:
```
git@github.com:wuduhren/leetcode-python.git
```

For example, go to https://github.com/wuduhren/leetcode-python. Click the `Code` and choose `SSH`. You will see git@github.com:wuduhren/leetcode-python.git.
