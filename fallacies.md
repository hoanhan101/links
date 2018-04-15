# Fallacies of Distributed Computing Explained

## References:

- http://www.rgoarchitects.com/Files/fallacies.pdf

## 8 fallacies

1. [The network is reliable](#the-network-is-reliable)
2. [Latency is zero](#latency-is-zero)
3. [Bandwidth is infinite](#bandwidth-is-infinite)
4. [The network is secure](#network-is-secure)
5. [Topology doesn't change](#topology-doesnt-change)
6. [There is one administrator](there-is-one-administrator)
7. [Transport cost is zero](#transport-cost-is-zero)
8. [The network is homogeneous](#the-network-is-homogeneous)

## The network is reliable

There are plenty of problems:
- Power failures
- Clients connect wirelessly
- Hardware problems
- External partners their side of connection is not under your direct control
- Security threads like DDOS

**Solution:**
- Hardware: think about redundancy and weigh the risk of failure
- Software: think about messages/calls getting lost

## Latency is zero

Latency is how much time it takes for data to move from one place to another.

Latency can be relatively good on a LAN--but latency deteriorates quickly 
when you move to WAN scenarios or internet scenarios.

**Solution:**
- Make as few as possible calls

## Bandwidth is infinite

Bandwidth which is how much data we can transfer during that time.

Bandwidth can grow really fast with big data.

**Solution:**
- Consider the volume of expected data

## Network is secure

It is far from being secure.

**Solution:**
- Build security into your solutions from day 1
- Evaluate security risks

## Topology doesn't change

It is usually out of control because it is changing constantly.

**Solution:**
- Try not to depend on specific endpoints or routes
- Either provide location transparency or service discovery
- Abstract the physical structure of the network (e.g: DNS)

## There is one administrator

In reality, the IT group usually has different administrators, assigned according
to expertise - databases, web servers, networks, Linux, Windows, so on.
There are also external entities.

**Solution:**
- Remember that administrators can constrain your options (administrators that sets 
disk quotas, limited privileges, limited ports and protocols and so on), and 
that you need to help them manage your applications.

## Transport cost is zero

These things can cost:
- Marshalling/serializing data
- Setting and running networks

**Solution:**
- Find cost-effective strategy

## The network is homogeneous

Most architects today are not naïve enough to assume this fallacy.

**Solution:**
- Do not rely on proprietary protocols
- Use standard technologies that are widely accepted
