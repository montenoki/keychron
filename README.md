# keychron

## How to build

1. Check out this repository.

   ```console
   $ git clone https://github.com/montenoki/qmk_keymaps.git qmk_keymaps
   ```

2. Check out [qmk/qmk_firmware](https://github.com/qmk/qmk_firmware/) repository in another place.

   ```console
   $ git clone https://github.com/qmk/qmk_firmware.git --depth 1 --recurse-submodules --shallow-submodules qmk
   ```

3. Create a symbolic link to this `keyball/` directory from [qmk/qmk_firmware]'s `keyboards/` directory.

   ```console
   $ ls
   keychron/ qmk/

   $ cd qmk/keyboards
   $ ln -s ../../qmk_keymaps/q1 keychron/q1/ansi_encoder/keymaps/ten
   $ ln -s ../../qmk_keymaps/q2 keychron/q2/ansi_encoder/keymaps/ten
   $ ln -s ../../qmk_keymaps/gmmk_pro gmmk/pro/rev2/ansi/keymaps/ten
   $ cd ..
   ```

4. `make` your Keyball firmware.

   ```console
   # Build q1 firmware
   $ make keychron/q1/ten

   # Build q2 firmware
   $ make keychron/q1/ten

   # Build q2 firmware
   $ make gmmk/pro/ten
   ```
