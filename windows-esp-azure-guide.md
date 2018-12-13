# ESP32 Development Guide: Windows 
Here is the steps on ESP32 guide developing on Windows.

# ESP Azure
The sample is from [esp azure](https://github.com/espressif/esp-azure).

## Setup Environment
* Download the [Toolchain](https://dl.espressif.com/dl/esp32_win32_msys2_environment_and_toolchain-20181001.zip) and then unzip it to `C:\`.
![Windows ESP32 Toolchain](/windows/1.png)

* Set the environment variable IDF_PATH.
  * The user profile scripts are contained in `C:/msys32/etc/profile.d/` directory.
  * Create a new script file in C:/msys32/etc/profile.d/ directory. Name it `export_idf_path.sh`.
  ![export_idf_path](/windows/2.png)
* Identify the path to ESP-IDF directory. It is specific to your system configuration and may look something like 'C:\msys32\home\user-name\esp\esp-idf'.
  * Add the export command to the script file, refer to the following case.
    ```
    export IDF_PATH="C:/msys32/home/user-name/esp/esp-idf"
    ```
* Open the mingw32.exe.
  ```
  Note: 
  This is very important. Please refer to the following steps.  
  ```
  * Open `C:\msys32\mingw32.exe`, not `msys2.exe`. Otherwise it will prompt python command cann't be found.
  ![mingw32.exe](/windows/3.png)
* Clone the [esp azure](https://github.com/espressif/esp-azure) via the following command.
  ```
  git clone --recursive https://github.com/espressif/esp-azure.git
  ```
  ```
  Note:
  Please don't forget the `--recursive` parameter while cloning source code.
  ```
  `Start to clone...`
  ![mingw32.exe](/windows/12.png)
  `Cloning...`
  ![mingw32.exe](/windows/13.png)
  `Completed clone`
  ![mingw32.exe](/windows/14.png)
* Configuration (Compliling & Serial Port).
  ![make 1 ](/windows/15.png)
* Navigate to `Serial flasher config -> Default serial port`.
  ![make 2](/windows/17.png)
   When serial port is configured.
  ![make 3](/windows/16.png)
  ```
  Note:
  On how to get the specific serial port. Open the Device Manager -> Ports.
  ```
  ![make 4](/windows/6.png)
* Configure Wifi & IoT Hub connection string.
  Navigate to `Example Configuration --->`.
  ![wifi configuration 1](/windows/18.png)
  Add your `WIFI` & `IoT Hub Connection String` information.
  ![wifi configuration 2](/windows/19.png)
  
* Save the configuration.
  ![save](/windows/20.png)
  
# Compiling & Flash
 * The step is similar to `hello world` sample, just using the following command.
  Comping & Flashing...
  ```
  make flash
  ```
  Then monitoring... 
  ```
  make monitor
  ```
  
  # References:
  * [esp guide](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html).
  * [esp windows setup](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/windows-setup.html).
  * [esp_azure](https://github.com/espressif/esp-azure).
  
  
  
