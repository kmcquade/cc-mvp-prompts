# System Data Block: default-deny-permissions-policy

- Source: inline

## Summary

Defines a default-deny policy with essential allowlisted permissions.

# Raw Prompt Text
(version ${NUM})

(deny default)

; Essential permissions

(allow process*)

(allow signal)

(allow sysctl-read)

(allow system-socket)

(allow mach*)

(allow ipc*)

(allow iokit*)

(allow user-preference-read)

(allow authorization-right-obtain)

(allow distributed-notification-post)
