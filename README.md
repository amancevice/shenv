# shenv

dotenv for your shell

## Install

Install with Homebrew:

```bash
brew tap amancevice/tap
brew install amancevice/tap/shenv
```

Add the following to your shell profile:

```bash
eval "$(shenv init -)"
```

## Usage

Create a `.env` file

```bash
cat <<-EOS > .env
VAR_1=val_1
VAR_2=val_2
VAR_3=val_3
EOS
```

Source the file with `shenv`:

```bash
shenv
```

By default, `shenv` will look for a file called `.env`, but you can override this with arguments:

```bash
shenv .env.development
```

Or pass multiple files:

```bash
shenv .env.1 .env.2
```

Files are sourced in the order you pass them.
