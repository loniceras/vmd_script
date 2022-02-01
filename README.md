# vmd_script
VMD 1.9.3 scripts for drawing beautiful Multiwfn graphs. Most of scripts were modified from Sobereva (http://sobereva.com/multiwfn/).

## Basic Configuration
1. Copy these `.vmd` files to installation directory of VMD 1.9.3.
2. Add following commands to `vmd.rc`.
    ```
    source showcub.vmd
    source showvib.vmd
    source showorb.vmd
    source showaim.vmd
    source showesp.vmd
    source showalie.vmd
    source showhirsh.vmd
    source showrdg.vmd
    source showigm.vmd
    source showanci.vmd
    ```

## Basic Usage
1. Generate required cub/pdb files by Multiwfn.
2. Move those cub/pdb files to the installation directory of VMD 1.9.3.
3. Open a new VMD window.
4. Input required command in VMD Command-Line Window.

| Multiwfn Function     | Command      | Required Files                            |
| --------------------- | ------------ | ----------------------------------------- |
| Read cub file         | `cub xxx`    | xxx.cub                                   |
| View vibration modes  | `vib xxx n`  | xxx.pdb, xxx.out                          |
| View orbitals         | `orb`        | orbital.cub                               |
| 2  AIM analysis       | `aim`        | mol.pdb, CPs.pdb, paths.pdb               |
| 12 ESP analysis       | `esp`        | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 ESP analysis       | `esppt`      | mol.pdb, vtx.pdb, surfanalysis.pdb        |
| 12 ALIE analysis      | `alie`       | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 LEA analysis       | `lea`        | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 HS analysis        | `hirshd`     | mapfunc.cub, surf.cub                     |
| 12 HS analysis        | `hirshr`     | mapfunc.cub, surf.cub                     |
| 20 RDG analysis       | `rdg`        | func1.cub, func2.cub                      |
| 20 IRI analysis       | `iri`        | func1.cub, func2.cub                      |
| 20 DORI analysis      | `dori`       | func1.cub, func2.cub                      |
| 20 IGM analysis       | `igminter`   | sl2r.cub, dg_inter.cub                    |
| 20 IGM analysis       | `igmintra`   | sl2r.cub, dg_intra.cub                    |
| 20 aRDG analysis      | `ardg`       | avgsl2r.cub, avgRDG.cub                   |
| 20 aRDG analysis      | `ardgtfi`    | thermflu.cub, dg_intra.cub                |
| 20 aIGM analysis      | `aigm`       | avgsl2r.cub, avgdg_inter.cub              |
| 20 aIGM analysis      | `aigmtfi`    | thermflu.cub, avgdg_inter.cub             |