# vmd_script
VMD 1.9.3 scripts for drawing beautiful Multiwfn graphs. Most of scripts were modified from Sobereva (http://sobereva.com/multiwfn/).

## Basic Configuration
1. Copy these `.vmd` files to installation directory of VMD 1.9.3.
2. Add following commands to `vmd.rc`.
    ```
    source showaim.vmd
    source showesp.vmd
    source showrdg.vmd
    source showigm.vmd
    ```

## Basic Usage
1. Generate required cub/pdb files by Multiwfn.
2. Move those cub/pdb files to the installation directory of VMD 1.9.3.
3. Open a new VMD window.
4. Input required command in VMD Command-Line Window.

| Multiwfn Function      | Command          | Required Files                |
| ---------------------- | ---------------- | ----------------------------- |
| 2 AIM                  | `aim`            | mol.pdb, CPs.pdb, paths.pdb   |
| 12 ESP                 | `esp`/`esp2`     | surf.cub, mapfunc.cub         |
| 12 ESP                 | `esppt`/`esppt2` | mol.pdb, vtx.pdb              |
| 12 ESP                 | `espext`         | surfanalysis.pdb              |
| 20 RDG                 | `rdg`            | func1.cub, func2.cub          |
| 20 IGM                 | `igminter`       | sl2r.cub, dg_inter.cub        |
| 20 IGM                 | `igmintra`       | sl2r.cub, dg_intra.cub        |