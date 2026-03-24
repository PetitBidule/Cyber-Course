Application: Nickel (Android APK Analysis)
Findings from strings.xml
1. API Endpoints Exposure

Extract:

https://api.nickel.eu/customer-banking-api

Risk:

Reveals backend structure
Enables API reconnaissance and endpoint mapping
Potential entry point for unauthorized testing or abuse
2. Authentication Endpoint

Extract:

https://api.nickel.eu/customer-authentication-api

Risk:

Identifies authentication service
Could be targeted for brute force or logic flaws
Useful for traffic interception and replay attacks
3. Production Environment Disclosure

Extract:

production

Risk:

Confirms connection to live environment
No separation from staging/dev reduces safe testing surface
Indicates real user data may be involved
4. Firebase Configuration

Extract:

https://application-client-nickel.firebaseio.com

Risk:

Potential misconfiguration could expose database
May allow unauthorized read/write if rules are weak
Enables cloud resource enumeration
5. Google API Key

Extract:

AIzaSyBTgztvImsUfMWDa41PCrDWAj7dmyIDhUg

Risk:

Can be abused if improperly restricted
May allow access to Google services (Maps, Firebase, etc.)
Useful for quota exhaustion attacks
6. OAuth Client ID

Extract:

717748501407-...apps.googleusercontent.com

Risk:

Identifies OAuth configuration
Can aid phishing or spoofed login flows
Useful in social engineering scenarios
7. Push Notification Identifier

Extract:

DDF11-D1BF9

Risk:

May allow unauthorized push message attempts
Could be used for spam or phishing notifications
Reveals third-party service usage
8. Crashlytics Build ID

Extract:

9ad6d741-4e10-4abd-9f12-163a0e3fb0b2

Risk:

Low sensitivity
Mainly used for crash reporting correlation
Minimal direct attack surface
Summary

The strings.xml file exposes:

Backend API endpoints
Cloud service configurations
Third-party integration identifiers

No critical secrets (e.g., passwords or private keys) were found, but the data enables:

Reconnaissance
Attack surface mapping
Potential misuse of misconfigured services