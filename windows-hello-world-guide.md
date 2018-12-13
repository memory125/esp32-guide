# ESP32 Development Guide: Windows 
Here is the steps on ESP32 guide developing on Windows.

# Hello World
The sample is copied from [esp_idf](https://github.com/espressif/esp-idf), [hello world](https://github.com/espressif/esp-idf/tree/23b6d40/examples/get-started/hello_world) sample is basic and simple sample to learn esp32 development.

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
  * Configuration (Compliling & Serial Port).
  ![make 1 ](/windows/4.png)
  * Navigate to `Serial flasher config -> Default serial port`.
  ![make 2](/windows/7.png)
   When serial port is configured.
  ![make 3](/windows/5.png)
  ```
  Note:
  On how to get the specific serial port. Open the Device Manager -> Ports.
  ```
  ![make 4](/windows/6.png)
  * Save the configuration.
  ![make 5](/windows/8.png)
# Compiling & Flash
 * Compiling...
  ![Compiling](/windows/9.png)
 * Flashing image to esp32 board.
  ![Flashing](/windows/10.png)
 * Run the sample `hello world`.
  ![Running hello world](/windows/11.png)
  
  # References:
  * [esp guide](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/index.html).
  * [esp windows setup](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/windows-setup.html).
  * [esp_idf](https://github.com/espressif/esp-idf).
  
  
  
