#Configuration in Manjaro-Xfce

- Configure Shadowsocks 

  ```bash
  $ vi shadowsocks.json
  ```

  ```json
  {
    "server":"",
    "server_port",
    "local_address",
    "local_port",
    "password",
    "timeout",
    "medthod",
    "fast_open"
  }
  ```

  ```bash
  $ sslocal -c shadowsocks.json -d start
  ```

  ​

- Laptop lid settings ignored

  ```bash
  $ xfconf-query -c xfce4-power-manager -p /xfce4-power-manager/logind-handle-lid-switch -s false
  ```

- Switch Display Manager from LightDM to SDDM

  ```bash
  $ sudo systemctl disable lightdm
  $ sudo systemctl enable sddm
  ```

- Configure Chrome in Xfce without desktop environment proxy manager

  ```bash
  $ chromium %U --proxy-server="socks5://127.0.0.1:1080"
  ```

  that will force chromium to use proxy server to Internet.

  and install SwithyOmega with Rule List URL: "https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt"

- Softwares

  - installed by yaourt
    - jetbrains-toolbox
    - typora
  - installed by pacman
    - docker/docker-machine/docker-compose
    - emacs
    - vim
    - thefuck
    - opencv
    - shadowsocks

- Configure bashrc

  add these to ./.bashrc

  ```bash
  alias vi='vim'
  alias dm='docker-machine'
  eval $(thefuck --alias)
  ```

  ​

  ​
