services = [
  'sway-session-pre.target',
  'sway-session.target',
  'sway.service',
  'wayland-session-pre.target',
  'wayland-session.target',
  'swayidle.service',
  'kanshi.service',
  'mako.service',
  'waybar.service',
]

in_services = [
]

conf = configuration_data({
  'prefix': get_option('prefix')
})

foreach srv : in_services
  configure_file(
    input: srv + '.in',
    output: srv,
    configuration: conf,
    install_dir: 'lib/systemd/user',
    install_mode: 'rw-r--r--',
  )
endforeach

install_data(services, install_dir: 'lib/systemd/user')
