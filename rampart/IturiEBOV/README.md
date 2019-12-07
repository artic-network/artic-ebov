# rampart-ebov
RAMPART protocol folder for EBOV

## Installing
Clone this repository:

```
git clone https://github.com/rambaut/rampart-ebov.git
```

Create conda environment and activate it:

```
```

## Running

Create run folder:

```
mkdir [run_name]
cd [run_name]
```

Where `[run_name]` is whatever you are calling todays run (as specified in MinKNOW).

Run RAMPART:

```
rampart --protocol ../rampart-ebov --basecalledPath ~/MinKNOW/data/reads/[run_name]/pass
```

`basecalledPath` should be set to whereever MinKNOW/guppy is going to write its basecalled files.
