<h4>1. Introduction</h4>
<p>
    In database security, two foundational concepts work hand-in-hand to protect data: <b>Authentication</b> and <b>Authorization</b>.
</p>
<ul>
    <li>
        <b>Authentication (AuthN):</b> The process of verifying a user's identity. It answers the question, <i>"Are you who you say you are?"</i> 
        Authentication acts as the primary gateway, requiring credentials (like a username and password) to allow entry into the system.
    </li>
    <li>
        <b>Authorization (AuthZ):</b> The process of determining what actions a verified user is permitted to perform. It answers the question, <i>"What are you allowed to do?"</i> 
        Once a user is authenticated, authorization ensures they can only access the data or commands they have been granted permission to use.
    </li> 
</ul>
<p>
    This experiment focuses <b>exclusively on Authentication</b>. By rigorously verifying identities, the system prevents unauthorized entry. 
    We will explore the configuration and management of user accounts and password policies to ensure 
    only legitimate users can access the database system.
</p>

<h4>2. Password Policies</h4>

<h5>2.1 User Account Management</h5>
<p>
    The first step in securing a database is creating specific user accounts. Unlike generic accounts, 
    individual accounts allow for precise tracking and accountability.
</p>
<ul>
    <li><b>Identification:</b> Every user is assigned a unique username.</li>
    <li><b>Verification:</b> Every account is secured with a password or another verification method to confirm identity.</li>
</ul>

<h5>2.2 Security and Password Policies</h5>
<p>
    Creating an account is only half the battle. To prevent unauthorized access via stolen or guessed 
    credentials, database systems enforce several security policies:
</p>
<ul>
    <li><b>Password Complexity:</b> Ensures passwords are not easily guessable by requiring a mix of characters 
    (uppercase, lowercase, numbers, and symbols).</li>
    <li><b>Password Expiry:</b> Regularly forcing users to update their passwords reduces the window of 
    opportunity for attackers who might have stolen old credentials.</li>
    <li><b>Account Lock Policies:</b> Automatically disabling an account after a certain number of failed 
    login attempts protects against "brute-force" attacks.</li>
</ul>

<h5>2.3 External and Multi-Factor Authentication</h5>
<p>
    Beyond local passwords, modern databases support external and more secure authentication mechanisms:
</p>
<ul>
    <li><b>External Services (LDAP/Active Directory):</b> Centralizes user management by allowing the database 
    to verify identities against a corporate directory service.</li>
    <li><b>Multi-Factor Authentication (MFA):</b> Requires two or more pieces of evidence (e.g., a password and a 
    mobile code) to verify identity.</li>
    <li><b>Certificate-Based Authentication:</b> Uses digital certificates (SSL/TLS) to verify both the client 
    and the server identities.</li>
</ul>

<h4>3. Understanding Login Behavior</h4>
<p>
    A critical part of managing a database is observing how it reacts during different authentication scenarios:
</p>
<ul>
    <li><b>Successful Authentication:</b> When correct credentials are provided, a session is established.</li>
    <li><b>Failed Attempt:</b> If incorrect credentials are used, the database denies entry and logs the attempt.</li>
    <li><b>Behavioral Observation:</b> Analyzing system responses to incorrect logins—such as delay increases 
    or locking triggers—is essential for recognizing and mitigating potential security threats.</li>
</ul>
