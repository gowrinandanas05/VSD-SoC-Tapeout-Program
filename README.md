


# Week 0 Report

## 📌 Task 1: GitHub Repository Creation and Video Summary



### 📝 Summary
The video explains the various stages to go from an idea in C language to a real chip used in electronics.

#### 🚀 Design Flow Steps:
- **Step 0 (O0 = O1) → Idea to C program**  
  - The chip’s functions are first written in C language.

- **Step 1 (O1) → C model specs**  
  - A specification stage where the chip’s behavior is modeled in C.  
  - Works like a simulation to understand the output of a chip for a given input.

- **Step 2 (O2) → RTL (Verilog model)**  
  - The chip design is written in Verilog (hardware description language).  
  - Represents the “soft copy” of the hardware, like circuit diagrams.  
  - Includes blocks such as:
    - **Processor (brain)**
    - **Peripherals/IPs (extra features like sensors, timers)**

- **Step 3 (O3) → Integration**  
  - Processor + Peripherals + Memory + Analog blocks combined into **SoC (System on Chip)**.  
  - Converted into a **Gate-Level Netlist** (electrical connections).

- **Step 4 (O4) → Final Chip**  
  - Fabricated silicon is used in real devices.

---

## 📌 Task 2: Tool Installation

### 💻 System Configuration
- **RAM:** 6 GB  
- **Hard Disk:** 50 GB  
- **OS:** Ubuntu 20.04+  
- **CPU:** 4 vCPU  

---

### ⚙️ 2.1 Installing Yosys
```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make
sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev
make config-gcc
make
sudo make install
````

<img width="851" height="562" alt="image" src="https://github.com/user-attachments/assets/64f50ca8-c512-455e-93f1-0b8e23cd7a49" />

---

### ⚙️ 2.2 Installing Icarus Verilog (Iverilog)

```bash
sudo apt-get update
sudo apt-get install iverilog gtkwave
```

<img width="940" height="629" alt="image" src="https://github.com/user-attachments/assets/2b655ba4-f4d9-4f4d-b07b-210a5cf5d217" />

---

### ⚙️ 2.3 Installing GTKWave

```bash
sudo apt-get update
sudo apt install gtkwave
```

<img width="940" height="548" alt="image" src="https://github.com/user-attachments/assets/9b43d55e-5573-4f3f-a9f0-45b1f99908f5" />

---

### ⚙️ 2.4 Installing Ngspice

```bash
tar -zxvf ngspice-37.tar.gz
cd ngspice-37
mkdir release
cd release
../configure --with-x --with-readline=yes --disable-debug
make
sudo make install
```

<img width="940" height="597" alt="image" src="https://github.com/user-attachments/assets/fd4e31f5-b64b-4111-bfaa-55ce8d455202" />

---

### ⚙️ 2.5 Installing Magic

```bash
sudo apt-get install m4
sudo apt-get install tcsh
sudo apt-get install csh
sudo apt-get install libx11-dev
sudo apt-get install tcl-dev tk-dev
sudo apt-get install libcairo2-dev
sudo apt-get install mesa-common-dev libglu1-mesa-dev
sudo apt-get install libncurses-dev
git clone https://github.com/RTimothyEdwards/magic
cd magic
./configure
make
sudo make install
```

<img width="940" height="508" alt="image" src="https://github.com/user-attachments/assets/8775b7a9-38bc-4a4c-a4bc-813b328a5fc6" />

---

### ⚙️ 2.6 Installing OpenLANE

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv python3-pip make git
sudo apt install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] \
https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io
sudo docker run hello-world
sudo groupadd docker
sudo usermod -aG docker $USER
sudo reboot
```

👉 After reboot:

```bash
docker run hello-world
git --version
docker --version
python3 --version
python3 -m pip --version
make --version
python3 -m venv -h
```

👉 Install OpenLANE:

```bash
cd $HOME
git clone https://github.com/The-OpenROAD-Project/OpenLane
cd OpenLane
make
make test
```

<img width="940" height="574" alt="image" src="https://github.com/user-attachments/assets/7a93313c-f2b8-46f6-a2b4-7ddc202ba069" />

---

## ✅ Final Notes

* All required tools installed successfully: **Yosys, Iverilog, GTKWave, Ngspice, Magic, OpenLANE**
* Verified system compatibility: **6GB RAM, 50GB HDD, Ubuntu 20.04+, 4vCPU**
* GitHub repository created and updated with installation details and screenshots.

<img width="940" height="534" alt="image" src="https://github.com/user-attachments/assets/2ada9eed-22b8-4a54-8875-794f5a811313" />

---

### 🎯 Completion Status

✅ Both Task 1 and Task 2 completed successfully

