# Maintainer: AlcyonX <votre.email@example.com>
# Contributor: Collaborateur <collaborateur.email@example.com>
# Package name: alpine-theme
# Version: 1.0.0
# Release: 1
# License: MIT
# Description: Thème Alpine pour Hyprland avec configurations pour Waybar, Wofi, et Hyprpaper
# URL: https://github.com/AlcyonX/alpine-theme
# Architecture: x86_64
# Depends on: hyprland
# Optional depends: waybar wofi hyprpaper
# Source: https://github.com/AlcyonX/alpine-theme/archive/refs/tags/v1.0.0.tar.gz
# SHA256 sum: à compléter une fois le paquet source téléchargé

pkgname=alpine-theme
pkgver=1.0.0
pkgrel=1
pkgdesc="Alpine theme for Hyprland with configurations for Waybar, Wofi, and Hyprpaper"
arch=('x86_64')
url="https://github.com/AlcyonX/alpine-theme"
license=('MIT')
depends=('hyprland' 'noto-fonts' 'waybar' 'dolphin' 'kitty' 'hyprlock' 'wofi' 'hyprpaper' 'ttf-jetbrains-mono-nerd')
source=("alpine-theme.tar.gz")
sha256sums=('SKIP')  # Remplacez par le checksum du paquet sourcez
# Fonction de construction

# Fonction d'installation
post_install() {
  cd "$srcdir/"
  
  # Installation des fichiers de configuration pour Waybar
  install -Dm644 waybar/config ~/.config/waybar/config
  install -Dm644 waybar/style.css ~/.config/waybar/style.css
  
  # Installation des fichiers de configuration pour Hyprland
  install -Dm644 hypr/hyprland.conf ~/.config/hypr/hyprland.conf
  
  # Installation des fichiers de configuration pour Wofi
  install -Dm644 wofi/style.css ~/.config/wofi/style.css
}

# Optionnel : Vous pouvez ajouter un script post-install pour rappeler à l'utilisateur de recharger ou d'appliquer les configurations
# post_install() {
#   echo "Les configurations pour Waybar, Wofi, Hyprland et Hyprpaper ont été installées. Veuillez recharger votre session."
# }
