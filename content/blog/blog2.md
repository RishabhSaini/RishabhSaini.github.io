---
title: "DevConf.cz 2023 Trip Report"

date: "2023-07-24"

tags: ["conference"]
---

Open source conferences expose you to the developer community which is where bleeding edge technology is often born. It helps get inspiration to join these communities and contribute. Conferences focused on FOSS is a great place to see the raw and organic enthusiasm about a project. Even if you don't plan to get involved in the field, it's educational and refreshing to see the different parts of the community.

Devconf.cz is an open conference with leading developers coming together to talk about the projects they are working on. This June of 2023, I got the opportunity to speak at DevConf.cz happening in Brno, Czech Republic. Getting to meet the community developers was invaluable. Being at the conference was a different experience than most of the conferences I had attended. It was an open source community conference by developers and targeted at developers. Being developer and tech oriented instead of customer and business oriented is what appealed to me the most. 

It felt empowering as an intern to be able to stand in the speaker position and show valuable work to a room full of industry experts. More than 45 people attended my talk, in–person and online, and I got at least 3 people to come up to me to ask further questions after the talk. Since the talk that I presented was on the feature I had implemented end-to-end entirely by myself, I had all the context to answer these questions.

However, the conference was so much more than the talk I gave. Listening to over 20 talks in a span of 3 days and interacting with their project team members gave me so much more than I had asked for. 

Here is a rundown of the most interesting talks and people I met:


{{< table_of_contents >}}
# Talks Given

## Hands on with fedora coreos
https://devconfcz2023.sched.com/event/1MYop/hands-on-with-fedora-coreos

Supported my team lead in the workshop

## Packing an OS in a container image intelligently
https://devconfcz2023.sched.com/event/1Mmbw/how-to-intelligently-pack-os-in-a-container-image

My talk <3

# Talks Related to my open-source project (ostree)

## OpenShift: OS customization as a bootable container
https://devconfcz2023.sched.com/event/1MYfv/openshift-os-customization-as-bootable-container

MCO side of Openshift layering

## Containers in a car
https://devconfcz2023.sched.com/event/1MYim/containers-in-a-car

Effort of RedHat In-Vehicle Operating system which uses ostree and rpm-ostree at its core along with Hirte to manage the microservice based infrastructure (based on systemd).

## Kairos: Linux meta distribution for edge
https://devconfcz2023.sched.com/event/1MYjD/meet-kairos-the-linux-meta-distribution-for-edge

# Talks Attended

## Confidential VMs in the cloud
https://devconfcz2023.sched.com/event/1MYg7/confidential-vms-in-the-cloud

“Data confidentiality” must also prevent the host from accessing data about the VM. This is achieved by encrypting the VM’s memory, the CPU state at runtime, storage volumes at rest and any communications while in transit. There is a compromise/tradeoff between encrypting different stages of the linux boot process and the speed of boot. Some parts of the chain must remain unencrypted to be able to decrypt the rest. The solution involved keeping the UEFI firmware unencrypted and using that to verify an encrypted unified kernel image. This keeps the root volume encrypted and the key to the root volume is revealed during the initramfs stage. The key is protected using hardware support: TPM-PCR policy (Trusted Platform Module - Platform configuration register).

## Building OKD Kubernetes Distro using tekton
https://devconfcz2023.sched.com/event/1MYg4/how-we-build-okd-kubernetes-distro-using-tekton

Building OKD (a community driven Kubernetes distribution along with SCOS (base linux operating system)) using Tekton CI/CD pipelines the cloud native way. It went through the entire build process to add developer and operations-centric tools on top of Kubernetes.

## Resiliency at the edge
https://devconfcz2023.sched.com/event/1MYid/resiliency-at-the-edge

It is hard to do hands-on-maintenance to a device deployed at edge. Hence, greenboot (part of fedora IOT) provides health checks on startup to ensure the system is functioning as expected. In case of a failure, it tries to reboot and rollback to a previous deployment until the problem is solved. These health checks are operating as systemd services which makes it easy for the developers to configure. This works with the help of a ostree booted system which offers capabilities of rolling back the system by using `chroot`.

## Correlation is not causation or is it?
https://devconfcz2023.sched.com/event/1MYkB/correlation-is-not-causation-or-is-it

Using risk difference, odds ratio and relative risk to measure the association between the exposure and the outcome. Relative risk measures the probability of an outcome in an exposed group to the probability of an outcome  in an unexposed group. Hence it was used to search for problems and their “actual” causes while running services in Kubernetes. Example: Clusters affected by Node filesystem space filling up.

## Forensic analysis of container checkpoints
https://devconfcz2023.sched.com/event/1MYjk/forensic-analysis-of-container-checkpoints

Container checkpointing allows to transparently save the state of a running container as a collection of image files to persistent storage. This can be used to reconstruct the processes inside a container and the data they have used at the time when the checkpoint was created. These tools can be used to examine the captured runtime state of all processes running in a container and to uncover evidence of malicious activity.

## OVN-Kubernetes: The new default CNI of OpenShift
https://devconfcz2023.sched.com/event/1MYfy/ovn-kubernetes-the-new-default-cni-of-openshift

A container network interface (CNI) helps configure network interfaces in Linux containers. It works by inserting a network interface into the container network namespace and making any necessary changes on the host. The OVN-k8s project, a successor to the OpenShift-SDN (software defined networking), is an abstraction layer on top of OVN (open virtual networking) and OVS (open virtual switch) to manage cluster networking traffic flows on the node.

## Privacy in the open-source - homomorphic encryption
https://devconfcz2023.sched.com/event/1MYjt/privacy-in-the-open-source-homomorphic-encryption

Homomorphic encryption allows a third party to perform computations on encrypted data, and get an encrypted result which can be handed over to the decryption key owner, without the third party being able to decrypt the data or the result for themselves. It can be used for enabling secure collaboration by protecting sensitive information, protecting intellectual property, ensuring data privacy and facilitating secure voting

## AI driven application optimization
https://devconfcz2023.sched.com/event/1MYd1/ai-driven-application-optimization

Bandit Algorithms (part of Reinforcement Learning)

## Stream processing at the edge with Apache Kafka
https://devconfcz2023.sched.com/event/1MYj1/stream-processing-at-the-edge-with-apache-kafka

Running Kafka at edge using Kubernetes and monitoring using prometheus

## Hirte: multi-node service orchestration for edge
https://devconfcz2023.sched.com/event/1MYjA/hirte-multi-node-service-orchestration-for-edge

Hirte is a multi-node service orchestrator for deterministic systems with limited resources such as edge devices

Material heavily intersects with ostree container native layering

## Bisection its not just for git
https://devconfcz2023.sched.com/event/1MYhE/bisection-its-not-just-for-git

simple multi-axis arbitrary bisection tool inspired by “git bisect”

## Wrap Up
https://devconfcz2023.sched.com/event/1MZGM/wrap-up-and-win-win-win

Stats on number of fruits eaten
More than 1000 people attended the conference 
