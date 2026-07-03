# HOWTO — heirloom-ancestors-darwin

## Fetching an ancestor for local study

```sh
mkdir -p /opt/heirloom/src/upstream-ancestors/
cd /opt/heirloom/src/upstream-ancestors/

# V7 (Bourne shell + toolchest ancestors)
curl -L -o v7.tar.gz \
    https://www.tuhs.org/Archive/Distributions/Research/Henry_Spencer_v7/v7.tar.gz
mkdir -p v7 && tar xzf v7.tar.gz -C v7/

# DWB 1.0 (doctools ancestor)
curl -L -o dwb_1.0.tar.gz \
    https://www.tuhs.org/Archive/Applications/Documenters_Workbench/dwb_1.0.tar.gz
mkdir -p dwb-1.0 && tar xzf dwb_1.0.tar.gz -C dwb-1.0/

# 32V (AT&T/BSD divergence)
curl -L -o 32v_usr.tar.gz \
    https://www.tuhs.org/Archive/Distributions/USDL/32V/32v_usr.tar.gz
mkdir -p 32V && tar xzf 32v_usr.tar.gz -C 32V/
```

## Comparing an ancestor against a Heirloom-Darwin repo

```sh
# Example: diff V7's sh against heirloom-sh-darwin's sh
diff -r /opt/heirloom/src/upstream-ancestors/v7/usr/src/cmd/sh/ \
        /opt/heirloom/src/sh/ | head -50

# Diff DWB 1.0's troff against heirloom-doctools-darwin's troff
diff -r /opt/heirloom/src/upstream-ancestors/dwb-1.0/troff/ \
        /opt/heirloom/src/doctools/troff/ | head -50
```

## Writing a comparison note

If you write a diff narrative worth publishing, put it in
`notes/heirloom-<repo>-vs-<ancestor>.md` in this repo and commit
alongside a manifest update.
