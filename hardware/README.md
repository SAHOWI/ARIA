\#Hardware



# Specification



## BareBone vs Refurbished Mini PC



## Mini PC Lenovo ThinkCentre M910x
### Upgrades

* CPU
* Memory
* Disk
* GraphicCard / GPU

## Operating System: CachyOS

### Installation of CachyOS

### Installing / ENabling NVIDIA Drivers

### Overcome CPU Throttling ( BD PROCHOT )
CAUTION: This might lead to overheating!!!

```bash
sudo pacman -S msr-tools
modprobe msr
sudo rdmsr 0x1FC
2c005d
sudo wrmsr 0x1FC 2c004d ## use output of rdmsr -1 
```




