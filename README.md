# pyscl-devel
Utilities to assist in sclo-python maintenance

## Full local sclo-python build in a mock chroot

    # Pending an rpm-list-builder release with CUSTOM_DIR support
    pipsi install https://github.com/ncoghlan/rpm-list-builder.git@issue-67-add-CUSTOM_DIR#egg=rpmlb
    git clone https://ncoghlan/pyscl-devel
    cd pyscl-devel/rpmlb
    rpmlb --custom-file sclorg-distgit-download.yml --download custom \
          --build custom --work-directory .working python-recipe.yml sclo-python

## sclo-python links

- [metapackage repo](https://github.com/ncoghlan/sclo-python/) (temporary, expected to move into https://github.com/sclorg-distgit)
- [Pre-release COPR builds](https://copr.fedorainfracloud.org/coprs/ncoghlan/sclo-python-preview/)
- TBD: CentOS Build System links
- TBD: softwarecollections.org links

## SCL resource Links

- [SCL definition overview](https://www.softwarecollections.org/en/docs/guide/#Creating_Your_Own_Software_Collections)
- [SCLo-SIG guide](https://wiki.centos.org/SpecialInterestGroup/SCLo#head-b408f06ad89fd3a67686f755eafac7ce310ee081)
- [RPM List Builder](https://github.com/sclorg/rpm-list-builder)
- [rh-pythonXY recipe file](https://github.com/sclorg/rhscl-rebuild-recipes/blob/master/python.yml)


## Current dependencies:

- RPM List Builder (install with `pip`, not packaged for Fedora)
- `scl-utils-build`, `mock`, `fedpkg`
- Jupyter notebook with the Python 3 kernel
