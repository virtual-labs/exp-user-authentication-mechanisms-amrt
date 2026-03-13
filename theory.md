<h4>1. Introduction</h4>
<p>
User authentication is the process of verifying the identity of a person accessing a database system. 
It ensures that only legitimate users can log in and perform operations. Authentication acts as the 
first line of defense, preventing unauthorized access and protecting sensitive data stored in the database.
<br><br>
Modern database systems provide multiple authentication methods, password policies, account controls, 
and security features that help administrators manage users effectively.
</p>

<p>
Authentication is the primary security gatekeeper for any database. It is the process of verifying a user's identity 
before granting any access to the data. This experiment focuses on manual configuration—the practical side of 
how administrators ensure that only authorized personnel can enter the system.
</p>

<h4>2. Key Authentication Mechanisms</h4>

<h5>2.1 User Account Management</h5>
<p>
The first step in securing a database is creating specific user accounts. Unlike generic accounts, 
individual accounts allow for precise tracking and individual permissions.
</p>
<ul>
    <li><b>Identification:</b> Every user is assigned a unique username.</li>
    <li><b>Verification:</b> Every account is secured with a strong password or another verification method.</li>
</ul>

<h5>2.2 Security and Password Policies</h5>
<p>
Creating an account is only half the battle. To prevent unauthorized access, database systems enforce several 
security policies:
</p>
<ul>
    <li><b>Password Complexity:</b> Ensures passwords are not easily guessable by requiring a mix of characters 
    (uppercase, lowercase, numbers, and symbols).</li>
    <li><b>Password Expiry:</b> Regularly forcing users to update their passwords reduces the window of 
    opportunity for attackers who might have stolen old credentials.</li>
    <li><b>Account Lock Policies:</b> Automatically disabling an account after a certain number of failed 
    login attempts protects against "brute-force" attacks (where an attacker tries thousands of passwords rapidly).</li>
</ul>

<h4>3. Understanding Login Behavior</h4>
<p>
A critical part of managing a database is observing how it reacts during different login scenarios:
</p>
<ul>
    <li><b>Successful Login:</b> When correct credentials are provided, a session is established, permitting 
    authorized operations.</li>
    <li><b>Failed Attempt:</b> If incorrect credentials are used, the database denies access and logs the attempt.</li>
    <li><b>Behavioral Observation:</b> Analyzing system responses to incorrect logins—such as delay increases 
    or locking triggers—is essential for recognizing and mitigating potential security threats.</li>
</ul>
