{{{
  "title": "Hairpin NATs",
  "date": "10-9-2015",
  "author": "Justin Lentz",
  "attachments": [],
  "contentIsHTML": false
}}}

### Hairpin NATs

This article discusses what a Hairpin NAT is and whether it is supported within CLC.

### Information

**Q - What is a hairpin NAT?**

A - Also referred to as "hairpinning", hairpinning describes a communication between two hosts behind the same NAT device using their mapped endpoint.

**Q - Does CenturyLink Cloud allow hairpinning or Hairpin NATs?**

A - YES (As of 2/2/16).

**Q - What does the traffic flow look like?**

A - Internal traffic destined to a IP address that resolves in a static mapping will have it’s source address NAT’d to that of the closest interface to the resolved endpoint.  This is to ensure that the traffic flow utilizes the firewall and does not result in a half open state because of a direct server return.

**Q - Can I still filter source addresses destined to my mapped endpoint?**

A - Yes but RFC1918 space will need to be added.

