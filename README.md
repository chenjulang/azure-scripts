lean3全环境一键解压可用包，的打包全过程（export这一行开系统代理，不用也可以。）：
python3 -m venv myenv
source myenv/bin/activate
pip install -r requirements.txt
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
python3 mk_bundle.py

完成后就会看到：
Making Linux archive
Making Windows archive
Making MacOS archive



# azure-scripts

This repo contains cron jobs for the following [leanprover-community](https://leanprover-community.github.io) tasks:

- update [mathlib](https://github.com/leanprover-community/mathlib)'s `lean-3.x.y` branch
- update mathlib's [linting](https://arxiv.org/abs/2004.03673) exception files
- delete stale olean archives from Azure
- update the [Lean+mathlib+vscodium bundles](https://leanprover-community.github.io/get_started.html#maybe-a-couple-of-nights)

## periodic bumps

The cron jobs in this repo will stop periodically without attention!
