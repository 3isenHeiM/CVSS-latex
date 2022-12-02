# CVSS-latex

This aims to become a LaTeX package allowing anyone to use and nicely print the CVSS ratings for a given CVSS string.

## Usage


### Direct forms

```latex
\cvssScore{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}
\cvssLevel{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}
\cvssLevelpretty{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:H/A:H}
\cvssTag{CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H}

The vuln has a  \textbf{\cvssLevel{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}}-level and we can output it inline.
```


![Direct forms](https://github.com/3isenHeiM/CVSS-latex/raw/main/img/direct-form.png)

### Imbricated Form

```latex
\cvssFrame{Low}
\category{9.9}

We can even combine them:
\category{\cvssScore{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}}
\cvssFrame{\category{\cvssScore{CVSS:3.1/AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}}}
```

![Imbricated forms](https://github.com/3isenHeiM/CVSS-latex/raw/main/img/imbricated-form.png)


## To-do

- [x] Fix the expansion error preventing nested commands like `\category{\computeCVSS{AV:L/AC:H/PR:N/UI:R/S:U/C:H/I:L/A:N}}`
- [x] Add support for CVSS complete string (starting wiht `CVSS:3.1`)
- [ ] Add CVSS values as variables (future CVSS version)
- [ ] Add support for full CVSS vector (temporal and environmental score)
- [x] Turn this into a latex package


## Licence
This package is licensed under the [LPPL-1.3c](https://www.latex-project.org/lppl/lppl-1-3c/).
The author of this package is [Pierre VIVEGNIS](https://ctan.org/author/vivegnis).
