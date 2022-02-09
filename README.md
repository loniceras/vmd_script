# vmd_script
These VMD 1.9.3 scripts are used to draw beautiful Multiwfn graphs. Most of scripts were modified from Sobereva (http://sobereva.com/multiwfn/), and all original scripts were available from the installation package of Multiwfn. The modified scripts are more robust and convenient than the original ones.

## Basic Configuration
1. Copy these `.vmd` files to installation directory of VMD 1.9.3.
2. Add following commands to `vmd.rc`.
    ```
    source showcub.vmd
    source showapt.vmd
    source showvib.vmd
    source showorb.vmd
    source showaim.vmd
    source showbas.vmd
    source showesp.vmd
    source showalie.vmd
    source showhirsh.vmd
    source showrdg.vmd
    source showigm.vmd
    source showanci.vmd
    ```

## Basic Usage
1. Generate required cub/pdb files by Multiwfn.
2. Move those cub/pdb/pqr/xyz files to the installation directory of VMD 1.9.3.
3. Open a new VMD window.
4. Input required command in VMD Command-Line Window.

| Multiwfn Function     | Command      | Required Files                            |
| --------------------- | ------------ | ----------------------------------------- |
| Read cub file         | `cub xxx`    | xxx.cub                                   |
| View atom properties  | `apt xxx`    | xxx.pqr                                   |
| View vibration modes  | `vib xxx n`  | xxx.xyz, xxx.out                          |
| View orbitals         | `orb`        | orbital.cub                               |
| 2  AIM analysis       | `aim`        | mol.pdb, CPs.pdb, paths.pdb               |
| 12 ESP analysis       | `esp`        | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 ESP analysis       | `esppt`      | mol.pdb, vtx.pdb, surfanalysis.pdb        |
| 12 ALIE analysis      | `alie`       | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 LEA analysis       | `lea`        | mapfunc.cub, surf.cub, surfanalysis.pdb   |
| 12 HS analysis        | `hirshd`     | mapfunc.cub, surf.cub                     |
| 12 HS analysis        | `hirshr`     | mapfunc.cub, surf.cub                     |
| 17 Basin analysis     | `basin`      | mol.pdb, attractors.pqr                   |
| 20 RDG analysis       | `rdg`        | func1.cub, func2.cub                      |
| 20 IRI analysis       | `iri`        | func1.cub, func2.cub                      |
| 20 DORI analysis      | `dori`       | func1.cub, func2.cub                      |
| 20 IGM analysis       | `igminter`   | sl2r.cub, dg_inter.cub                    |
| 20 IGM analysis       | `igmintra`   | sl2r.cub, dg_intra.cub                    |
| 20 aRDG analysis      | `ardg`       | avgsl2r.cub, avgRDG.cub                   |
| 20 aRDG analysis      | `ardgtfi`    | thermflu.cub, dg_intra.cub                |
| 20 aIGM analysis      | `aigm`       | avgsl2r.cub, avgdg_inter.cub              |
| 20 aIGM analysis      | `aigmtfi`    | thermflu.cub, avgdg_inter.cub             |

## Useful Tips
- Use the command `helpp` to get commands available in the current script.
- In some scripts, the display styles (colors, materials), isosurface values, lower and upper limits of color scale can be changed via commands, using `helpp` for more information.
- In some scripts, the labels can be added via commands like `labcp all` and removed via command `labcp no`. Some useful information such as critical point indexes, atoms properties, ESP extrema, ALIE extrema, LEA extrema are given in the labels.
- In script `apt xxx`, cubes can be added via commands like `cubadd cubname` and removed via command `cubdel`. Files request: cubname.cub
- In script `apt xxx`, orbitals can be added via commands like `orbadd 1 3` and removed via command `orbdel`. Files request: orb000001.cub, orb000002.cub, orb000003.cub
- In script `aim` and `basin`, basins can be added via commands like `basinadd 1 3` and removed via command `basindel`. Files request: basin0001.cub, basin0002.cub, basin0003.cub
- In script `rdg`, `iri`, `dori`, `igminter`, and `igmintra`, critical points and topology paths can be added via commands `aimadd`. Files request: CPs.pdb, paths.pdb