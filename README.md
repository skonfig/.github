# cdist

This is the [community maintained](https://github.com/cdist-community)
fork of [ungleich](https://github.com/ungleich)'s [cdist](https://github.com/ungleich/cdist)
(after [f061fb1](https://github.com/ungleich/cdist/commit/f061fb168ddacc894cb6e9882ff5c8ba002fadd8)).

Work is split between four repositories:

* **cdist** - documentation, project wide issues etc (this repository).
* [cdist-core](https://github.com/cdist-community/cdist-core) - implementation of the **cdist core**.
* [cdist-conf](https://github.com/cdist-community/cdist-conf) - **essential** explorers and types.
* [cdist-extra](https://github.com/cdist-community/cdist-extra) - **non-essential** explorers, types, scripts, tools etc.

Difference between essential and non-essential? Explorers and types which are
used to manage state of the operating system (modify files and directories,
install packages, manage services, etc.) and are not strictly related to some
specific piece of software are considered essential.

## Getting Started

Since this fork is still in early stages, there will be no versioned releases for now.

Everything is expected to be used straight from the repositories.

We are currently targeting cdist power users who already know what they are doing, so expect some rough edges.

### Step 1: Clone repositories

```sh
cd ~/Where/YOU/keep/your_repos/
git clone https://github.com/cdist-community/cdist-core
git clone https://github.com/cdist-community/cdist-conf
git clone https://github.com/cdist-community/cdist-extra
```

### Step 2: Add `cdist` to `$PATH`

```sh
ln -s "$PWD/cdist-core/bin/cdist" "$HOME/.local/bin/cdist"
```

### Step 3: Create configuration directory and file

```sh
mkdir "$HOME/.cdist"
cat > "$HOME/.cdist.cfg" << EOF
[GLOBAL]
conf_dir = $HOME/.cdist:$PWD/cdist-extra:$PWD/cdist-conf
EOF
```
