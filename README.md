## check_or

Run multiple checks and return the best observed status. This is useful for,
as an example, monitoring a service where the process may have one of several
names. Simply run both process checks without caring which one works.

### Usage

    $USER1$/check_or "$USER1$/check_procs -c 1: -C vmware-guestd" \
                     "$USER1$/check_procs -c 1: -C vmtoolsd"

    -> PROCS OK: 1 process with command name 'vmtoolsd'

