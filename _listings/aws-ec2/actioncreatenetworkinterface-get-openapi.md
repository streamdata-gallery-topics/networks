---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Create Network Interface
  version: 1.0.0
  description: Creates a network interface in the specified subnet.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AttachNetworkInterface:
    get:
      summary: Attach Network Interface
      description: Attaches a network interface to an instance.
      operationId: attachnetworkinterface
      x-api-path-slug: actionattachnetworkinterface-get
      parameters:
      - in: query
        name: Description
        description: A description for the network interface
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Ipv6AddressCount
        description: The number of IPv6 addresses to assign to a network interface
        type: string
      - in: query
        name: Ipv6Addresses.N
        description: One or more specific IPv6 addresses from the IPv6 CIDR block
          range of your subnet
        type: string
      - in: query
        name: PrivateIpAddress
        description: The primary private IPv4 address of the network interface
        type: string
      - in: query
        name: PrivateIpAddresses.N
        description: One or more private IPv4 addresses
        type: string
      - in: query
        name: SecondaryPrivateIpAddressCount
        description: The number of secondary private IPv4 addresses to assign to a
          network interface
        type: string
      - in: query
        name: SecurityGroupId.N
        description: The IDs of one or more security groups
        type: string
      - in: query
        name: SubnetId
        description: The ID of the subnet to associate with the network interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Network Interface
  /?Action=CreateNetworkAcl:
    get:
      summary: Create Network Acl
      description: Creates a network ACL in a VPC.
      operationId: createnetworkacl
      x-api-path-slug: actioncreatenetworkacl-get
      parameters:
      - in: query
        name: CidrBlock
        description: The IPv4 network range to allow or deny, in CIDR notation (for
          example                172
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Egress
        description: Indicates whether this is an egress rule (rule is applied to
          traffic leaving the subnet)
        type: string
      - in: query
        name: Icmp
        description: 'ICMP protocol: The ICMP or ICMPv6 type and code'
        type: string
      - in: query
        name: Ipv6CidrBlock
        description: The IPv6 network range to allow or deny, in CIDR notation (for
          example                2001:db8:1234:1a00::/64)
        type: string
      - in: query
        name: NetworkAclId
        description: The ID of the network ACL
        type: string
      - in: query
        name: PortRange
        description: 'TCP or UDP protocols: The range of ports the rule applies to'
        type: string
      - in: query
        name: Protocol
        description: The protocol
        type: string
      - in: query
        name: RuleAction
        description: Indicates whether to allow or deny the traffic that matches the
          rule
        type: string
      - in: query
        name: RuleNumber
        description: The rule number for the entry (for example, 100)
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC ACL
  /?Action=CreateNetworkAclEntry:
    get:
      summary: Create Network Acl Entry
      description: Creates an entry (a rule) in a network ACL with the specified rule
        number.
      operationId: createnetworkaclentry
      x-api-path-slug: actioncreatenetworkaclentry-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: NetworkAclId
        description: The ID of the network ACL
        type: string
      responses:
        200:
          description: OK
      tags:
      - VPC ACL
  /?Action=CreateNetworkInterface:
    get:
      summary: Create Network Interface
      description: Creates a network interface in the specified subnet.
      operationId: createnetworkinterface
      x-api-path-slug: actioncreatenetworkinterface-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: NetworkInterfaceId
        description: The ID of the network interface
        type: string
      responses:
        200:
          description: OK
      tags:
      - Network Interface
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---