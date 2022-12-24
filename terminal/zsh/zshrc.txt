# Enable Powerlevel10k instant prompt. Should stay close to the top of ~/.zshrc.
# Initialization code that may require console input (password prompts, [y/n]
# confirmations, etc.) must go above this block; everything else may go below.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="/home/teacode/.oh-my-zsh"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes

#ZSH_THEME="robbyrussell"
#ZSH_THEME="agnoster"
ZSH_THEME="powerlevel10k/powerlevel10k"

# Set list of themes to pick from when loading at random
# Setting this variable when ZSH_THEME=random will cause zsh to load
# a theme from this variable instead of looking in $ZSH/themes/
# If set to an empty array, this variable will have no effect.
# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

# Uncomment the following line to use case-sensitive completion.
# CASE_SENSITIVE="true"

# Uncomment the following line to use hyphen-insensitive completion.
# Case-sensitive completion must be off. _ and - will be interchangeable.
# HYPHEN_INSENSITIVE="true"

# Uncomment the following line to disable bi-weekly auto-update checks.
# DISABLE_AUTO_UPDATE="true"

# Uncomment the following line to automatically update without prompting.
# DISABLE_UPDATE_PROMPT="true"

# Uncomment the following line to change how often to auto-update (in days).
# export UPDATE_ZSH_DAYS=13

# Uncomment the following line if pasting URLs and other text is messed up.
# DISABLE_MAGIC_FUNCTIONS="true"

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to disable auto-setting terminal title.
# DISABLE_AUTO_TITLE="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
# COMPLETION_WAITING_DOTS="true"

# Uncomment the following line if you want to disable marking untracked files
# under VCS as dirty. This makes repository status check for large repositories
# much, much faster.
# DISABLE_UNTRACKED_FILES_DIRTY="true"

# Uncomment the following line if you want to change the command execution time
# stamp shown in the history command output.
# You can set one of the optional three formats:
# "mm/dd/yyyy"|"dd.mm.yyyy"|"yyyy-mm-dd"
# or set a custom format using the strftime function format specifications,
# see 'man strftime' for details.
# HIST_STAMPS="mm/dd/yyyy"

# Would you like to use another custom folder than $ZSH/custom?
# ZSH_CUSTOM=/path/to/new-custom-folder

# Which plugins would you like to load?
# Standard plugins can be found in $ZSH/plugins/
# Custom plugins may be added to $ZSH_CUSTOM/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git zsh-autosuggestions)

source $ZSH/oh-my-zsh.sh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"
source /home/teacode/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh


## CUSTOM ALIASES

# SYSTEM
alias cls="clear"
alias rmrf="rm -rf"

# SSH
alias debian="ssh teacode@192.168.117.132"
alias centos="ssh teacode@192.168.117.130"

# DIRECTORIES
alias home="cd ~"
alias desktop="cd ~/Desktop/"
alias html="cd /var/www/html/"
alias nginx="cd /var/www/nginx"

# GIT
alias ga.="git add ."
alias ga="git add"
alias gaa="git add ."
alias gb="git branch"
alias gc="git commit"
alias gck="git checkout"
alias gcl="git clone"
alias gcm="git commit -m"
alias gd="git diff"
alias gi="git init"
alias gl="git log"
alias glp="git log-pretty"
alias gm="git merge"
alias gpl="git pull"
alias gplbit="git pull bitbucket master"
alias gplgit="git pull github master"
alias gplo="git pull origin"
alias gplom="git pull origin master"
alias gps="git push"
alias gpsbit="git push bitbucket master"
alias gpsgit="git push github master"
alias gpso="git push origin"
alias gpsom="git push origin master"
alias gr="git reset"
alias grfl="git reflog"
alias grh="git reset --hard"
alias grhh="git reset --hard HEAD"
alias grm="git rm"
alias grs="git reset --soft"
alias grv="git remote -v"
alias gs="git status"

# COMPOSER
alias ci="composer install"
alias cmpref="composer dump-autoload"
alias cu="composer update"

# LARAVEL
alias rfl="composer dumpautoload & php artisan optimize & php artisan cache:clear & php artisan view:clear"
alias pa="php artisan"
alias padbs="php artisan db:seed"
alias pakg="php artisan key:generate"
alias pam="php artisan migrate"
alias pamf="php artisan migrate:fresh"
alias pamfs="php artisan migrate:fresh --seed"
alias pamkc="php artisan make:controller"
alias pamkcmp="php artisan make:component"
alias pamkcr="php artisan make:controller -r"
alias pamkmdl="php artisan make:model"
alias pamkmg="php artisan make:migration"
alias pamkmm="php artisan make:model -m"
alias pamkmmc="php artisan make:model -m -c"
alias pamkmmcr="php artisan make:model -m -c -r"
alias pamkr="php artisan make:resource"
alias pamkrc="php artisan make:resource"
alias pamks="php artisan make:seeder"
alias pams="php artisan migrate --seed"
alias parl="php artisan route:list"
alias pas="php artisan serve"
alias pash="php artisan serve --host"
alias pasp="php artisan serve --port"
alias pat="php artisan tinker"
alias pav="php artisan --version"
alias punit=".\vendor\bin\phpunit"


# ANGULAR
alias nggc="ng generate component --skipTests"
alias nggcs="ng generate component"
alias nggd="ng generate directive --spec=false"
alias nggds="ng generate directive"
alias nggs="ng generate service --spec=false"
alias ngs="ng serve"
alias ngsa="ng serve --aot"

# NPM
alias ni="npm install"
alias nu="npm update"
alias nrb="npm run build"
alias nrd="npm run dev"
alias nrs="npm run serve"
alias nrw="npm run watch"

# DOCKER
alias dc="docker-compose"
alias dcx="docker-compose exec"
alias dk="docker"
alias dkim="docker image"
alias dkimls="docker image ls"
alias dkims="docker images"
alias dkimsa="docker images -a"
alias dkll="docker kill"
alias dksp="docker system prune"
alias dkspa="docker system prune -a"
alias dps="docker ps"
alias dpsa="docker ps -a"
alias rmcn="docker container rm"
alias rmim="docker image rm"


# To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
