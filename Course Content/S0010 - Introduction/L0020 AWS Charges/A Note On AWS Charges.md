#1 Slide on deploy/destroy

This has two advantages

1. Charges are generally according to the amount you consume. By destroying the system you can stop the charges-meter ticking : your costs will immediately stop going up.
2. You are given $100 of credit with a new account. Once your credits are used up you can "hop" to another account easily.

# Email accounts

Each AWS account requires a unique email account, so we will create a new gmail account as part of our system setup.

This email address will be our "root" email address.

Once logged in, we will create an AWS "IAM" user ...

Each user requires their own email address.

We will use gmail's "PLUS ADDRESSSING" feature for this.

For instance if the root address is uptickart@gmail.com

We will create an AWS user called "dev" and tell AWS that their email address is uptickart+dev@gmail.com

We will not need to create a new email address ... emails of the format uptickart+xxxx@gmail.com will be rooted to the root gmail account.
