# vpc2vpc : Site to Site VPN Tunnels for Virtual Private Clouds (VPC)
This tool will automate the process of setting up EC2 instances to build site to site VPN tunnels between VPCs in your AWS cloud.  Use this at your own risk.  It hasn't been fully tested and is in the early stages of development.

## Requirements

You will need to have the following in order to use vpc2vpc:

* Java 1.6+
* AWS Access Key and Secret Access Key
* Two or more VPCs to connect

## Installation

1. Extract the downloaded tar.gz file in your preferred location
2. Set the bin directory under the extracted vpc2vpc directory in your PATH
3. Set the JAVA_HOME variable pointing to JRE/JDK you wish to use
4. Set the AWS\_ACCESS\_KEY\_ID & AWS\_SECRET\_ACCESS\_KEY environment variables

## Creating a vpc2vpc Connection

To create a vpc2vpc connection, you can specify the VPCs you'd like to connect using CIDR notation or VPC ID.  You can also specify the specific public subnet you wish to launch the VPN instances by CIDR notation or Subnet ID.  See the examples below for details:

### Examples

	# Create a connection between VPCs using CIDR notation
	$ vpc2vpc create 10.1.0.0/16 10.2.0.0/16

	# Create a connections between three VPCs using CIDR notation
	$ vpc2vpc create 10.1.0.0/16 10.2.0.0/16 10.3.0.0/16

	# Create connections between three VPCs but specify a specific subnet for the VPN instances in the 10.1.0.0/16 VPC
	$ vpc2vpc create 10.1.0.0/24 10.2.0.0/16 10.3.0.0/16

## Listing vpc2vpc Connections

	$ vpc2vpc list

## Deleting vpc2vpc Connections

	$ vpc2vpc delete

