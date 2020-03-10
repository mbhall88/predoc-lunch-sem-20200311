+++
weight = 200
+++
{{% section %}}


# Tool of the week

---


## Click

```py
import click

@click.command()
@click.option(
    "-i",
    "--input",
    required=True,
    type=click.Path(exists=True, file_okay=True, dir_okay=False, readable=True,),
    help="The file to do x with.",
)
@click.option(
    "-o",
    "--output",
    required=True,
    type=click.Path(
        exists=False, file_okay=True, dir_okay=False, writable=True, allow_dash=True
    ),
    help="The path to write the output to.",
    default="-",
    show_default=True,
)
def main(input: str, output: str):
    do_bioinformatics(input, output)

```

```shell
$ python main.py --input in.fa -o out.txt
```

---

## EBI slide template

GitHub: **mbhall88/reveal-hugo-ebi**


<img src="images/screenshot.png"  height="500" width="800" style="border: none;">

---

> Always code as if the person who ends up maintaining your code will be a violent psychopath who knows where you live.   
>     - Martin Golding

{{% /section %}}
