# SimpleAlgorithm: Documentation

## Usage

- To load the package, add the following command to the preamble:

```latex
\usepackage{SimpleAlgorithm}
```

- When loading the package, you can also specify the following options:
    - `equation`: This option turns on the equation mode. In this mode, all
      algorithms are treated like usual equations.

- The `SimpleAlgorithm` environment has several optional arguments, which
  can be specified using the standard `keyword=value` syntax:
    - `title`: The title of the algorithm.
    - `label`: The label assigned to the algorithm for future referencing. Note
      that you must not explicitly use the `\label` command for this.
    - `width`: The width of the algorithm (default: `0.85\linewidth`).

- By default, each algorithm is numbered (using the `algorithm` counter). If
  you want to disable the numbering for a particular algorithm, use the
  `SimpleAlgorithm*` environment.

- Each `SimpleAlgorithm` environment must consist of one or several groups
  (`AlgorithmGroup` environments), which can be thought of as the major
  parts of the algorithm description (Input, Initialization, Main Loop,
  Return, etc.). By default, the groups are not visually separated from each
  other. If needed, you can use the `\AlgorithmGroupSeparator` command to
  add a separator (the horizontal line).

- The `AlgorithmGroup` environment has one optional argument specifying the
  title of the group.

- To specify the steps of the algorithm inside a group, use the
  `AlgorithmSteps` environment. It has the same syntax as the usual
  `enumerate` list with the only difference that you should use the
  `\AlgorithmStep` command instead of `\item`. Similarly to standard lists,
  you can nest the `AlgorithmSteps` environment if needed.

- It is possible to label individual steps for future referencing. To assign
  a label, simply add the corresponding `\label` command immediately after
  `\AlgorithmStep`.

## Example

See [this LaTeX source file](Example/src/Main.tex).