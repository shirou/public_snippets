---
title: signal caught and graceful shutdown
tags:
  - golang
---
ctx, cancel := context.WithCancel(context.Background())
defer cancel()

// Spawn a goroutine and listen for a signal.
signalChan := make(chan os.Signal)
go func() {
        for s := range signalChan {
                switch s {
                case syscall.SIGTERM:
                        logger.Warn("SIGTERM caught. start to graceful shutdown")
                        cancel()
                }
        }
}()
signal.Notify(signalChan, syscall.SIGTERM)
