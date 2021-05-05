# ZSH + Powerlevel10k + Fuzzy History

## MacOS

	brew install zsh

	brew install romkatv/powerlevel10k/powerlevel10k
	echo "source $(brew --prefix)/opt/powerlevel10k/powerlevel10k.zsh-theme" >>~/.zshrc
	p10k configure

	brew install fzf
	$(brew --prefix)/opt/fzf/install	
