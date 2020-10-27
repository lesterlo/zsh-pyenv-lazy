# zsh-pyenv-lazy

A zsh plugin for lazy loading of pyenv.
The initial `eval "$(pyenv init -)"` is executed the first time `pyenv` is called.

If `ZSH_PYENV_LAZY_VIRTUALENV` is set to `true`, also call `eval "$(pyenv virtualenv-init -)"`.

About the PYENV_VIRTUALENV, 
In the pyenv virtualenv [github page](https://github.com/pyenv/pyenv-virtualenv). the author said this is [optional](https://github.com/pyenv/pyenv-virtualenv/blob/master/README.md#L37) for adding this line `eval "$(pyenv virtualenv-init -)"`.

Since running virtualenv-init, my mac zsh shell goes slow again. So, I disable it .

## Installation

### zgen

Update your `~/.zshrc` with the following line:

```sh
zgen load davidparsson/zsh-pyenv-lazy
```

### oh-my-zsh

```sh
git clone https://github.com/lesterlo/zsh-pyenv-lazy.git ~/.oh-my-zsh/custom/plugins/pyenv-lazy
```

Then, in your `~/.zshrc`, add `pyenv-lazy` to your `plugins` variable.

## N.B.

If your theme calls out to `pyenv` when constructing the prompt
(e.g. using the `pyenv` element in powerlevel9k),
pyenv will still be loaded immediately.

`
