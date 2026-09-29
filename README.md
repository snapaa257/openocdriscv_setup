# OpenOCD Riscv Setup
This is a guide to setup openocd_rsicv for the OpenOCD remote-bitbang.
Main openocd_riscv repo can be followed to set everything up.

## Steps
**1. Installing dependencies**
At point of setup, ubuntu OS used.
  ```bash
   sudo apt-get install libtool automake libusb-1.0.0-dev texinfo libusb-dev libyaml-dev pkg-config
  ```

**2. Clone repo**
   ```bash
    git clone https://github.com/SpinalHDL/openocd_riscv.git
   ```
Move into clone repo
   ```bash
    cd openocd_riscv
   ```

**3. Run bootstrap**
   ```bash
    ./bootstrap
   ```

**4. Run configure**
   ```bash
    ./configure --enable-dummy
   ```

In the case step 4 fails, run
   ```bash
    ./configure --enable-dummy --disable-dependency-tracking
   ```

### OR

   ```bash
    sudo apt-get update && apt-get install -y build-essential 
   ```
then rerun

   ```bash
    ./configure --enable-dummy
   ```

**5. Run make**
   ```bash
    make
   ```

**6. Verify**
   ```bash
    ./src/openocd
   ```
If that is done and it shows then setup done.

## Additional
OpenOCD Riscv main repo:
https://github.com/SpinalHDL/openocd_riscv.git

