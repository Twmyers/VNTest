

# 2018 Build 15 Release Notes

## Bug Fixes

We modified the behaviour of
Value
Navigator Licensing to not persist a Windows Registry key for
Machine ID. This could cause issues when deploying
Value
Navigator over Citrix, where an incorrect Machine ID was copied
to a different application server in a Citrix farm.
