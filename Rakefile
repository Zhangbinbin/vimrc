desc "deploy vimrc"
task :deploy do
  # Bundle and scripts
  system 'git clone http://github.com/gmarik/vundle.git ~/.vim/bundle/vundle'
  system 'cp .vimrc .gvimrc ~/'
  system 'vim +BundleInstall +qa'
  system 'cd ~/.vim/bundle/Command-T/ruby/command-t/; rvm system do ruby extconf.rb; make clean; make; cd -'

  # snipmate-snippets
  system 'git submodule init; git submodule update'
  system 'cd snipmate-snippets/; rake deploy_local; cd -'
end
