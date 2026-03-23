# Meeting One Agenda
Agenda for meeting one 3/13/2026

Topics that need to be covered:

- Introductions
- Club Constitution
- Responsibilities of officers
- Environment Setup
    - WSL install
    - Basic Linux? Probably won't have time. Can maybe provide beginner guide and ask people to read it over.
    - Python intro and install
    - Anaconda install. Virtual Environments and installing packages(???)
    - Github account creation and git installation
    - IDE install

## Introductions
- Go around the room and introduce ourselves.
- Name, major, career goals.
- Introduce Officers
- (This is really so Advisors can get acquainted with current members. Everyone pretty much already knows eachother).

## Club Constitution
[link](https://github.com/TCC-South-Data-Science-Club/org-docs/blob/main/constitution.md) 

## Responsibilities of Officers
List the Responsibilities of Officers

View club constitution for more detailed overview

- President (April):
    - Oversee all meetings
    - Set and monitor organization goals
    - Delegate tasks
    - Keep in contact with advisors and other RSO's
    - Register club for service activities 

- Senator (Fred):
    - Attend SGA and represent club at all SGA meetings
    - Welcome new members and guests
    - Announce importatn club updates
    - Assist the club in completing service activities

- Vice President (Camron):
    - Assist President with administrative duties and assume those duties in the absence of the President
    - Complete tasks as delegated by the President
    - Aid in overseeing club officer structure

- Secretary (Chris):
    - Keep accurate and detailed records of all meetings and affairs
    - Coordinate preperation and distribution of club flyers, handouts, and publications
    - Manage attendance (sign in sheet) at all meetings and events
    - Organizes and monitors the club calendar
    - Assist in creating meeting agendas

- Project Manager (Titus):
    - Assist the President in creating and executing a timeline for all projects
    - Plan and develop project scope
    - Work with club members to ensure projects are being completed on time
    - Monitor project progress and set deadlines
    - Aid general membership in overcoming obstacles that arise throughout a project's development
    - Manage and track tickets in CRM

## Environment Setup
This will be the bulk of the first meeting. Walk club members through installation of WSL, Python, Anaconda, Github/Git, and VSCode. I will need a volunteer bc I do not have Windows \:P

More detailed guide can be found on the Org github README.md

- WSL (Windows Subsystem for Linux)
    - Control Panel > Programs > Turn Windows Features On Or Off > Windows Subsystem for Linux
    - restart
    - Powershell -> wsl --install
    - Microsoft Store -> Ubuntu 24.04 LTS 
    - Launch Ubuntu. Follow prompt to create new Linux user.

- Python
    - Standalone Python is not necessary to install as it is contained within the Anaconda install

- Anaconda 
    - curl -O https://repo.anaconda.com/archive/Anaconda3-2025.12-2-Linux-x86_64.sh
    - bash ~/Anaconda3-2025.12-2-Linux-x86_64.sh

- Github
    - Have all members create a github account with 2FA and invite them to the github organization

- Git
    - sudo apt install git
    - git config --global user.name "Name"
    - git config --global user.email "email"
    - git config --global core.editor "vim"
    - git config --global core.autocrlf input
    - git config --global core.safecrlf true

- IDE install
    - Guide everyone through installing VSCode. Download installer from [Microsoft website](https://code.visualstudio.com/download)

