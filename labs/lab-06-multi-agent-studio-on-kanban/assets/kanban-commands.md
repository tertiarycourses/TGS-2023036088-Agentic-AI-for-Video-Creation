# Kanban commands — Lab 6

The kanban-video-orchestrator skill writes most of this for you. Use these to
check and steer.

    hermes kanban init                      # create the default board
    hermes kanban list                      # see tasks and status
    hermes kanban watch                     # live view in the terminal
    hermes gateway start                    # runs the dispatcher
    hermes gateway status
    hermes dashboard                        # web board: comment, assign, drag

Create a task and a dependent task by hand:

    hermes kanban create "Write EP02 script" --assignee scriptwriter --json
    hermes kanban create "EP02 storyboard" --assignee scriptwriter --parent <id>

Schedule — create, then pause until approved:

    hermes cron create "every tuesday 9am" "Start the next Kopi & Coins episode from the series backlog" --skill kanban-video-orchestrator --name kopi-weekly
    hermes cron pause kopi-weekly
    hermes cron list
