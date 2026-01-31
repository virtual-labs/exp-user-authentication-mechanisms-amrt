<h4>1. Introduction</h4>
<p>
User authentication is the process of verifying the identity of a person accessing a database system. 
It ensures that only legitimate users can log in and perform operations. Authentication acts as the 
first line of defense, preventing unauthorized access and protecting sensitive data stored in the database.
<br><br>
Modern database systems provide multiple authentication methods, password policies, account controls, 
and security features that help administrators manage users effectively.
</p>

<h4>2. Importance of User Authentication</h4>
<p>User authentication is essential for:</p>
<ul>
    <li>Preventing unauthorized access to the database.</li>
    <li>Protecting confidential and sensitive information.</li>
    <li>Enforcing accountability by identifying who performed an action.</li>
    <li>Supporting auditing and compliance.</li>
    <li>Enabling secure multi-user access in enterprise systems.</li>
</ul>

<h4>3. Types of Authentication Mechanisms in Database Systems</h4>

<h5>3.1 Password-Based Authentication</h5>
<p>
This is the most common authentication method. The user provides a username and password, the 
database compares the provided password with the stored hash, and access is allowed only if they match.
</p>
<ul>
    <li><b>Benefits:</b> Simple to configure.</li>
    <li><b>Limitations:</b> Vulnerable if weak passwords are used.</li>
</ul>

<h5>3.2 OS-Based Authentication</h5>
<p>
In Operating System (OS) authentication, the database trusts the OS login. If the user is authenticated 
at the OS level, they can access the database automatically.
</p>
<p><b>Examples:</b></p>
<ul>
    <li>Oracle OS authentication (OPS$users)</li>
    <li>SQL Server Windows Authentication</li>
</ul>
<p><b>Advantages:</b></p>
<ul>
    <li>Centralized control</li>
    <li>Stronger security (no DB passwords)</li>
</ul>

<h5>3.3 Multi-Factor Authentication (MFA)</h5>
<p>
MFA provides an additional security layer by requiring multiple proofs of identity:
</p>
<ul>
    <li>Password (what the user knows)</li>
    <li>OTP/Token (what the user has)</li>
    <li>Biometrics (what the user is)</li>
</ul>

<h5>3.4 Certificate-Based Authentication</h5>
<p>
Users authenticate using digital certificates instead of passwords. This is commonly used in systems 
requiring encryption, SSL, and high-level security.
</p>

<h5>3.5 External Authentication (LDAP / Active Directory)</h5>
<p>
External authentication integrates database systems with LDAP, Kerberos, or Active Directory for 
centralized identity management and reduced password duplication.
</p>

<h4>4. User Account Management in Databases</h4>

<h5>4.1 Creating Users</h5>
<p>
Database administrators create user accounts using commands like:
</p>
<ul>
    <li><b>Oracle:</b> CREATE USER</li>
    <li><b>SQL Server:</b> CREATE LOGIN + CREATE USER</li>
    <li><b>PostgreSQL:</b> CREATE ROLE + GRANT</li>
</ul>
<p>Each user receives:</p>
<ul>
    <li>Username</li>
    <li>Authentication method (password, OS, certificate, etc.)</li>
    <li>Default schema or tablespace</li>
</ul>

<h5>4.2 Granting Permissions</h5>
<p>
After user creation, privileges must be assigned:
</p>
<ul>
    <li>System privileges (CREATE SESSION, CREATE TABLE)</li>
    <li>Object privileges (SELECT, INSERT, UPDATE)</li>
    <li>Role-based privileges (admin, analyst, developer)</li>
</ul>
<p>This follows the <b>principle of least privilege</b>.</p>

<h4>5. Password Policies</h4>
<p>
Database systems enforce password policies to improve security.
</p>

<h5>5.1 Password Length & Complexity</h5>
<ul>
    <li>Minimum length</li>
    <li>Uppercase/lowercase letters</li>
    <li>Numbers and special characters</li>
</ul>

<h5>5.2 Password Expiry</h5>
<p>Passwords must be changed after a set period.</p>

<h5>5.3 Account Locking</h5>
<p>Accounts lock after repeated failed login attempts.</p>

<h5>5.4 Password History</h5>
<p>Prevents reuse of older passwords.</p>

<h5>5.5 Failed Login Tracking</h5>
<p>Tracks and audits failed login attempts.</p>

<h4>6. Login Behavior and Session Management</h4>

<h5>6.1 Successful Login</h5>
<p>
If credentials match, the database creates a session and allows actions based on granted privileges.
</p>

<h5>6.2 Failed Login</h5>
<p>Failed login reasons include:</p>
<ul>
    <li>Incorrect credentials</li>
    <li>Account locked or expired</li>
    <li>Password policy violations</li>
</ul>

<h5>6.3 Account Lockout</h5>
<p>Occurs when too many failed attempts exceed allowed limits.</p>

<h5>6.4 Session Timeout</h5>
<p>Inactive sessions automatically expire to prevent misuse.</p>
