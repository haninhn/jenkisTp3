pipeline {
agent any
triggers {
pollSCM('H/5 * * * *')
}
environment {
DOCKERHUB_CREDENTIALS = credentials ( ’0000’)
IMAGE_NAME_SERVER = ’[ username ]/ mern-server’
IMAGE_NAME_CLIENT = ’[ username ]/ mern-client’
}
stages {
stage ( ’Checkout’) {
steps {
git branch : ’main’ ,
url: 'git@github.com:haninhn/jenkisTp3.git',
credentialsId : ’b3BlbnNzaC1rZXktdjEAAAAACmFlczI1Ni1jdHIAAAAGYmNyeXB0AAAAGAAAABDgFQBILY
5jMIjIFdU9zUGIAAAAGAAAAAEAAAIXAAAAB3NzaC1yc2EAAAADAQABAAACAQDDCKrn9+Sf
gUaijpChnYvt7f2cA0MKHvax5GGzA6qR9qNkv2p9LBFWYCALqURzdD+pUGOxGmsEDJWvTN
E4KM+ZQ0s0889GqRCJ6u0LQGmXiVOJIwEsMBgBxpEYg/wluUS47F0h6TveT4VY0R/bdFp4
joN/gk2pg6nqh4XRNkFxOjdOpE2RqVi8Qr/LSBA+YlVWqjQxl12+p9xxMJETf957G4PpGR
ptsVxc3J8o3W228rKzK9WC7w0YwR/BKR1dLIC8On4cxhOHbRHh8xC5WljIgqyvikg27K8J
EVmhCKw5okIeTu2YEPimojyjQ2EOwLj5EmnoZj45gLQolUihN1A3zpws52+jCkm6k7K3VG
D8B4lzghj0NCy5MTWCSm6sd8SmwsEe2GINFjECKRns9ZaniLeVhwx9wRVrU81hsINHjPhO
X4PpJzjIxDNwxDY2WbVN5cLIutCTgXrXBjD/w37LRlViAxypuWP/iH9nCNKUHTuy92bQxK
dNSyPYhjCg9ECtOPWpPRk5/opt28rY5HpsraoUXIrHyOy3Q0s5fe3b7RKpp0QezrV/6Qw3
New8L8xzias1GuVNNwqjzI/fm2S8WSJnpnlSIRmPbr7/H6HnyBzu79mm4aeSKETCEsdUX1
p0ioJU2dzFq320cbHWkT3hXx1h8Yort+MEkCTIKGrJwwAAB1BJaYyW1bUm0SEudiGaMpWp
4qWI2bNPBq7aCUYfi1T9Gi9PpXj+XOzCZhTLuVBIDgjfH9TCJxCquMb7QfnhlgLdMzfaWe
g+3jKeJNHkYRW2oi2fOgnnVsLVLdtB6OCBsSR5O5i2RC3TX7xytzEKnR6WOqJxCb+sCY6n
Ezq2cZtChVJmn4+P4e3OOmfdvCkIRpns6eh62jcWmkSvJ90a3ZHXCfzHtB3FdzYdaaTSOR
dxQufvYYFffjTbqXnfDuQ4jOzGigLfC8aGXxncILDO+IdhdlTf051nn4wo+Gkd8q7Fpe5d
1iB9GCH8ByJ/KKzNVrNwk7qnjE9HRpnLSSM89wdaY5azQyq57Hn2eihwf1gVWR03hziMtt
vwQmD+YroXYTG6CAtp9AN69Q8sxC3jF2xlH/6vJYh7uCGrHdlPl+ExLVJVi0Ag24rGx3JS
KvLmp5uw6yuXafACOIaZoxoauqkfmKD/zcchKUC0HfiUXD+ffvug9Nqcn2vjWu1MWIcZt7
7DlGFWyZHn3kVmyL8s/sj4GHEVwVF62f5iBYu6dDx9bwC+DybWYp3vIr6BCEHItfE8Rid/
pBHGt0SkxWEkvnKFFgVsqFv4FcGBPMTI2h62YFIyfxB7TbKCTXTzJQ+NeXqVTrpxgCpkY5
ePJHkUC/QZGk6bIKkj5zM3f8oamUZZpAecZu/sqHqZ9Xkf1G/xu6jFqipBALYiWUKODzOY
GfXJs4fV5W8WOpvoTa4n6XZjl20eYhaHt4PIzMCIMIvyoKJe1Jc79kVrlxN2DT0SrUa8EG
lRkILVlXZQ8fK2TtIxqZoHeRI/oPRghOhxblfZSn5JVU7ovMYlv3NkEc7+qzMFEJbGAz88
hfQDVRQdEJyBFmfgJWCqgYeNwqpg2Esz2CTE3XdSZh0O04Mlfu6TXUIkkP8mZnDohiuzAQ
7ehTwkfk0SH7k6bV1ZY1ybhUaiRDbttRTnMNoQPN/1c/G1JHUbyjUbxlRAA/Y7qJ7zVIlg
oNtfULImZ/cA1CC9fVzgtnKfkhFGBHH79bjYsFFfnl2o1ygHTRcraFYfMb/KbWeQkS78xC
7gSmIK9Tm2THIRJuMV/yrtPdUZWKh8MLtIwoSFYbXGjOg8e6HP3PiIsdlESRG5bXv7s22U
ZvG2MCsRdRk1J1+RLAogUbaZF90LsrEMTaoDjZ+rEFAixh1T8ZkKhAA7yYlRIhSughWwYH
wJQkU9Q++FzzwTNGpSeWB6Lt3AO5TDwErMhJc4Gfltll0vdiUjRIDw4JrwJqu+QQw8Mq4F
0968DtETE0RFBEznnblxypfmZvsNu8wRpTack2UN9YnzqLEKTJ5FXvj24VtJmQalkTd6GN
nwOj7zTIwMeNC8s/mKpxPaJVYDZvNw4WwHyAdh1/Ha60c3xP8kuEn0aTANh2pEIBZ0/vrl
zk/PcPOw3DdBBVsTMn6gj7woVM3M24z7AX171oJk2T89Fy6uNGJwLcdpZBfGIvkop3xQ9b
7CplUNOrs1kZ8uRaiojE2/x3cdrKvMKvrBoWdwtcfsKIX69x8kHEfQgP4JHpv2Hei1s+9Q
VzcJ7925u84c4AkJJkd4L3R8M1Yo4HLrUrc940GpRSep1y45LQzkBQorfLaPn45oXoKp+O
eNzJ0Iyipw7KLL3Bt+vW1bBs0oA820WdCRu+XpJlzTz5MN6F6cRWGkTaNzt13yOx5HeUSW
x7g1gjYsMlsWGlo//TtKj4GT5iJyK37uJO4Y+CwngAcnBOxQXZpF6wEBNnLVogGrNQ76Nk
oKWxgr2BuHJzEJAhAiHQbEhIvEtcieBzrAenRMaqNduSgQuzPHEO7OI676Aah8Km9TDm0f
HE8dnh3YjBIA+ZbeoZwJAd08qWk1nG7lcNen0GKxvzw1zirjWwXPUBMkiDFHpkw+MvIMyl
7h1PybWmiKwbTGZ3mUZqnkR/f0E+sQLAa3suGOabY/dDHv66pdZ4eCeTAZpgUwBvEgY74J
SlIudqE2mPyJx4V5XWKxz2vaYntP/IRvPPgl4w6TdUSh+RW6M79Y3Llsyqe5CenybawYTQ
WDIqyPbddwxOTuuQ8DUhl/ZMOQhBFDPqeArwjZKegNQNvASDrHuxw0lvPWpCkiTAlLceiy
IcEbDFn2ZQZGULas1o5fDgjeyfepkGPopv7CmQqwcT00v68dKfdw/a7fQfw+3H86qo16Xx
tp1DWXeERJ7VI3Lxo9HbG4ZtpEQMAIyfYskducQBSYmdbYOJZH/Rh52P9sNbPSr9wEfvXk
5FY3Q05lhLZuyADQABNWQ2fOhO7w5kspuJnMtCC3KkHm9HqxwT9cRz0m2D2nIM8Z+ljb4B
BopTwZvUQHpcOeXleIwuh3D8AtMtVqn3Tsb7E4pRMYx8ctiuhbbJjsm1JHN+i3Q3tn3Kv4
eR1wxEglyu8PBPPhZpU2z/PVwTrb2soGvtpBMyr43n0vMP/5W1iy2qbGP+OjwNET7V+xUC
823xCQWLPMCwEoEyBiPCi+UwM=
’
}
}
stage ( ’ Build Server Image ’) {
steps {
dir ( ’ server ’) {
script {
dockerImageServer = docker . build (" $ {
IMAGE_NAME_SERVER }")
}
}
}
}
stage ( ’ Build Client Image ’) {
steps {
dir ( ’ client ’) {
script {
dockerImageClient = docker . build (" $ {
IMAGE_NAME_CLIENT }")
}
}
}
}
stage ( ’ Scan Server Image ’) {
steps {
script {
sh """
docker run -- rm -v / var / run / docker . sock
:/ var / run / docker . sock \\
aquasec / trivy : latest image -- exit - code 0
-- severity LOW , MEDIUM , HIGH , CRITICAL
\\
$ { IMAGE_NAME_SERVER }
"""
}
}
}
stage ( ’Scan Client Image’) {
steps {
script {
sh """
docker run -- rm -v / var / run / docker . sock
:/ var / run / docker . sock \\
aquasec / trivy : latest image -- exit - code 0
-- severity LOW , MEDIUM , HIGH , CRITICAL
\\
$ { IMAGE_NAME_CLIENT }
"""
}
}
}
stage ( ’Push Images to Docker Hub ) {steps {
script {
docker . withRegistry ( ’ ’ , " $ {DOCKERHUB_CREDENTIALS}") {
dockerImageServer . push ()
dockerImageClient . push ()
}
}
}
}
}
}