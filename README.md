# Canto v5.0.0 Upgrade
- [v5.0.0 release](https://github.com/Canto-Network/Canto/releases/tag/v5.0.0)
- [changelog](https://github.com/Canto-Network/Canto/compare/v4.0.0...v5.0.0)

# Changes
#### State machine breaking
- introduction of CSR module
- store upgrade to add CSR store key

# Upgrade instructions
### 1. Vote on software upgrade proposal
1. Proposal will be submitted at 11am EST on Wednesday Jan. 25th
2. If successful, proposal will halt chain at block `2668948`, at approximately 12:10pm EST on same day

### 2. When chain halts for upgrade, pull and install new binary
1. `cd Canto`
2. `git pull`
3. `git checkout v5.0.0`
4. `make install`

### 3. Verify Cantod version
```
# should be v5.0.0
cantod version

# commit should be "869fec6044ce3c3dc5e41f0fbee88a230d813008"
cantod version --long
```

### 4. Restart node
1. stop node: `sudo systemctl stop cantod.service`
2. restart node: `sudo systemctl start cantod.service`
