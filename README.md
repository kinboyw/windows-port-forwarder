# windows-port-forwarder
## ⚡ A Simple PowerShell Port Forwarding Tool for WSL2 ⚡

This PowerShell script, `PortForwarder.ps1`, allows you to easily create, manage, and delete port forwarding rules within your Windows environment for accessing services running inside your WSL2 distribution. It leverages the `netsh` command to establish port mappings and provides a user-friendly interface for convenient interactions. 🎉

### Features

- **Add Port Mapping:**  Create new port forwarding rules, specifying the local listening port, local listening IP address, remote forwarding port, and remote forwarding IP address (defaults to WSL2 IP). 🗺️
- **Remove Port Mapping:** Delete existing port forwarding rules by selecting the rule from a displayed list. 🗑️
- **List Port Mappings:** View the current list of established port forwarding rules. 📑
- **Retry Port Mapping:** Remap a selected port forwarding rule by deleting and re-adding it, providing the opportunity to update forwarding settings. 🔄
- **User-Friendly Interface:**  Interactive menus guide you through the process, requiring minimal input from the user. 🧭

### ScreenShots
![](https://img.kinboy.wang/file/e4f6974c80d7eb3013c50.png)

![](https://img.kinboy.wang/file/bcaafeaa975f9c6151bf3.png)

### Requirements

- PowerShell installed. 💻
- PowerShell execution policy set to `RemoteSigned` or `Unrestricted` or `Bypass`. 🔐
- WSL2 distribution installed if you want to forward local port to WSL2. 🐧

### Installation

1. **Copy the `PortForwarder.ps1` script to your desired location.** 📥
2. **Open PowerShell as administrator.** 🔐
3. **Navigate to the directory where you saved the script.** 📁
4. **Run the script by typing `.\PortForwarder.ps1` and pressing Enter.** 🏃

### Usage

The script presents a main menu with options for:

1. **Create new port forward:**  Add a new port mapping. ➕
2. **Delete port forward:**  Remove an existing port mapping. ➖
3. **List port forward:** View all current port mappings. 👀
4. **Remap port forward:** Update the settings of an existing port mapping. 🔁
5. **Exit:** Close the script. 🚪

### Example

To forward port `8080` on your Windows machine to port `80` running on your WSL2 distribution, you would:

1. Choose option **1 (Create new port forward)** from the main menu.
2. Enter the local listening port as `8080`.
3. Enter the local listening IP address (optional, default is `0.0.0.0`).
4. Enter the remote forwarding port as `80`.
5. Enter the remote forwarding IP address (optional, default is the WSL2 IP).

### Note

- The script assumes your WSL2 distribution is running and has a service listening on the specified port. 
-  Remember to disable port forwarding rules when you no longer need them. 
-  For more information on port forwarding in Windows, refer to the official Microsoft documentation. 📖

### Contributing

Contributions to improve this script are welcome. Feel free to fork the repository and submit pull requests. 🙌

---
