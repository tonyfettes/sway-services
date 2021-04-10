services = [
  'targets/wayland-session-pre.target',
  'targets/wayland-session.target',
  'targets/desktop-environment.target',
  'targets/graphical-session-timers.target',
  'sway/sway.service',
  'sway/swayidle.service',
  'wob/wob.socket',
  'wob/wob.service',
  'wob/wob-mkfifo.service',
  'kanshi.service',
]

install_data(services, install_dir: 'lib/systemd/user')
