# QurantineTale
Experimenting with available covid-19 related apis

Added rules in pre-commit to avoid any direct commits to master branch
	Add the below lines to .git/hooks/pre-commit:
		master="$(git rev-parse --abbrev-ref HEAD)"
		if [ "$branch" = "master" ]; then
			echo "You can't commit directly to master branch"
			exit 1
		fi
