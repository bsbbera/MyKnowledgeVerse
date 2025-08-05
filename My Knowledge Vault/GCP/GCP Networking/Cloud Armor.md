---
tags: [gcp, networking, security, waf, ddos_protection]
---

# Cloud Armor

Cloud Armor is Google Cloud's Web Application Firewall (WAF) and DDoS protection service that helps protect your applications and websites from common web attacks and distributed denial-of-service attacks. It operates at the edge of Google's network, providing protection before traffic reaches your resources.

## Key Features

- **DDoS Protection**: Protect against volumetric attacks
- **Web Application Firewall (WAF)**: Protect against web attacks
- **Edge Security**: Protection at Google's network edge
- **Pre-configured Rules**: OWASP Top 10 protection
- **Custom Rules**: Create your own security rules
- **Geo-based Access Control**: Block or allow by country
- **IP-based Access Control**: Block or allow by IP address
- **Named IP Lists**: Manage groups of IP addresses
- **Rate Limiting**: Protect against brute force attacks
- **Adaptive Protection**: ML-based attack detection
- **Google Cloud Armor Managed Protection Plus**: Advanced protection
- **Integration with Load Balancing**: Protect HTTP(S) load balancers
- **Logging and Monitoring**: Track security events

## Protection Types

Cloud Armor provides several types of protection:

### DDoS Protection
- **Infrastructure Layer (L3/L4)**: Protect against volumetric attacks
- **Application Layer (L7)**: Protect against application-layer attacks
- **Always-on Protection**: Automatic protection
- **Scalable Defense**: Google-scale protection

### Web Application Firewall
- **OWASP Top 10**: Protection against common web vulnerabilities
- **Cross-Site Scripting (XSS)**: Detect and block XSS attacks
- **SQL Injection**: Detect and block SQL injection attacks
- **Remote File Inclusion**: Prevent unauthorized file access
- **Local File Inclusion**: Prevent local file access
- **Remote Code Execution**: Block code execution attempts

## Security Policy Components

Cloud Armor security policies consist of:

- **Rules**: Define what traffic to allow or deny
- **Priority**: Determine rule evaluation order
- **Match Conditions**: Criteria for rule application
- **Actions**: Allow, deny, or redirect traffic
- **Preview Mode**: Test rules before enforcement
- **Logging**: Record rule matches

## Rule Types

Cloud Armor supports several rule types:

- **Pre-configured WAF Rules**: Ready-to-use security rules
- **Custom Rules**: Create your own rules
- **Geo-based Rules**: Block or allow by country
- **IP-based Rules**: Block or allow by IP address
- **Layer 7 Rules**: HTTP(S) header and content rules
- **Rate Limiting Rules**: Limit request rates
- **Named IP Lists**: Manage groups of IP addresses
- **Expression-based Rules**: Complex rule conditions

## Expression Language

Cloud Armor uses a powerful expression language for rules:

- **Request Headers**: Match HTTP headers
- **Request Method**: Match HTTP methods
- **Request URI**: Match URI patterns
- **Source IP**: Match source IP addresses
- **Region Code**: Match geographic regions
- **Logical Operators**: AND, OR, NOT
- **Regular Expressions**: Pattern matching
- **Functions**: String and IP functions

## Deployment Models

Cloud Armor can be deployed in several ways:

- **Global HTTP(S) Load Balancer**: Protect global applications
- **Regional HTTP(S) Load Balancer**: Protect regional applications
- **External Application Load Balancer**: Protect external applications
- **Internal Application Load Balancer**: Protect internal applications
- **Google Cloud Armor Managed Protection Plus**: Advanced protection

## Adaptive Protection

Cloud Armor Adaptive Protection uses machine learning:

- **Anomaly Detection**: Identify unusual traffic patterns
- **Attack Signatures**: Recognize attack patterns
- **Automatic Rule Generation**: Create rules automatically
- **Attack Alerts**: Notify about detected attacks
- **Recommended Rules**: Suggest protection rules

## Integration with Google Cloud

Cloud Armor integrates with several Google Cloud services:

- **Cloud Load Balancing**: Protect load balancers
- **Cloud CDN**: Protect cached content
- **Cloud Logging**: Log security events
- **Cloud Monitoring**: Monitor security metrics
- **Security Command Center**: Centralized security management
- **Cloud Armor Managed Protection Plus**: Advanced protection

## Use Cases

- **Public-facing Applications**: Protect web applications
- **E-commerce Websites**: Protect online stores
- **API Endpoints**: Protect API services
- **Content Sites**: Protect media and content
- **Enterprise Applications**: Protect business applications
- **High-profile Targets**: Protect against targeted attacks
- **Compliance Requirements**: Meet security standards
- **Multi-cloud Protection**: Protect resources across clouds

## Best Practices

1. **Layer Defense**: Combine multiple rule types
2. **Start in Preview Mode**: Test rules before enforcement
3. **Use Pre-configured Rules**: Leverage ready-to-use protection
4. **Implement Rate Limiting**: Prevent abuse
5. **Monitor and Tune**: Adjust rules based on traffic
6. **Enable Logging**: Track security events
7. **Use Adaptive Protection**: Leverage ML-based detection
8. **Document Security Policies**: Maintain documentation
9. **Regular Reviews**: Update rules periodically
10. **Incident Response Plan**: Prepare for attacks

## Comparison with Other WAF Solutions

| Feature | Cloud Armor | AWS WAF | Azure WAF |
|---------|-------------|---------|-----------|
| Edge Protection | Google's edge | CloudFront edge | Azure edge |
| DDoS Protection | Built-in | AWS Shield | Azure DDoS Protection |
| Pre-configured Rules | Yes | Yes | Yes |
| Custom Rules | Yes | Yes | Yes |
| Geo-blocking | Yes | Yes | Yes |
| Rate Limiting | Yes | Yes | Yes |
| ML-based Protection | Adaptive Protection | Limited | Limited |
| Integration | GCP services | AWS services | Azure services |
| Pricing Model | Pay-as-you-go | Pay-as-you-go | Pay-as-you-go |

## Related Topics
- [[GCP Networking]]
- [[Cloud Load Balancing]]
- [[Cloud CDN]]
- [[Security Best Practices]]
- [[DDoS Protection]]
