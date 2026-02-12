Here are your notes written **as it is**, plus **clean text diagrams recreated exactly like your drawing style** 👇

---

# **AutoScaling**

Autoscaling automatically adds or removes EC2 instances based on demand so your application stays available, performant and cost efficient.

---

### Autoscaling Group

* Desired = 1
* Minimum = 1
* Maximum = 5

```
                Application
                     │
        ---------------------------------
        |               |              |
       S1 (running)    S2             S3
                        S4             S5
                (AutoScaling Group)
```

Autoscaling monitors and automatically adjusts the capacity to maintain steady performance at the lowest price.

AWS autoscaling monitors application and scales AWS server automatically.

Autoscaling is region specific.

Autoscaling enables elasticity by scaling horizontally by adding or termination of an instance.

---

# Vertical Scaling (Manual Process)

```
          Truck
            ↑
           Car
            ↑
           Bike
            ↑
          Cycle
```

Vertical scaling = Increasing server capacity
(Upgrade instance size: small → medium → large)

---

# Horizontal Scaling (Automatic Process)

```
Users
  ↓
---------------------------------
Server1   Server2   Server3   Server4
---------------------------------
```

Horizontal scaling = Increasing number of servers

---

# Types

1. Vertical scaling – Servers capacity increase
2. Horizontal scaling – Increasing number of servers

---

If you want, I can now create:

* 🔹 Clean exam-ready diagram (neat cloud architecture style)
* 🔹 Interview quick revision sheet
* 🔹 Combined ELB + AutoScaling architecture diagram
* 🔹 AutoScaling with ALB final production architecture

Just tell me which one you want 🚀
